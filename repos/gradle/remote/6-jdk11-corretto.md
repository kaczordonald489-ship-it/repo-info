## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:4f2a239eb5942e497e072beee42b8aa38394661755da3184a42d82cd940b5f40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:4e8c27e125851bececcb2e45f9168a75000bf040c30729c2fdc36890bbc0635c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401435686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a9491b01566749a053ae9fb4040731aee43ac04a58e6950b97e8799b146e66`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:08:09 GMT
ARG version=11.0.29.7-1
# Thu, 20 Nov 2025 20:08:09 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:08:09 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:08:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 20 Nov 2025 20:48:31 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 20:48:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 20:48:31 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 20:48:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 20:48:31 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 20:48:31 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 20:48:31 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 20 Nov 2025 20:48:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 20 Nov 2025 20:48:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 20:48:35 GMT
USER gradle
# Thu, 20 Nov 2025 20:48:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 20:48:35 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42846af0e68a9e71193e1276692c1d9b6881acbae7fd1a7caccd4e873c30374b`  
		Last Modified: Thu, 20 Nov 2025 20:28:08 GMT  
		Size: 153.3 MB (153313068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f141d96f92842ebc9e1729a225219c987bbd4960d010da13811aaad83a681b9e`  
		Last Modified: Fri, 21 Nov 2025 05:53:37 GMT  
		Size: 86.0 MB (86023994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e1d0173a1b8233f22748018beed341de56e9d993ded7ad3b677484da7993e`  
		Last Modified: Thu, 20 Nov 2025 21:34:06 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f29849751e71281f1c1da2461e24157e2a55e8a279373bc8f5e0947cb5bfa8a`  
		Last Modified: Fri, 21 Nov 2025 05:53:44 GMT  
		Size: 107.7 MB (107696646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c816f3298f3a8d36c9834fe8cd3e577d514fd16347395cfd486dce99e80a87`  
		Last Modified: Thu, 20 Nov 2025 21:34:07 GMT  
		Size: 431.3 KB (431279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0a1aad01fef025ebc10e9cb46ee4fd099d97321e1012bf353acbdbff4cc69ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eddbb4526d425ea456a0f5b7fc96d9118f6336b0a2e3a89afb65ca433dd160`

```dockerfile
```

-	Layers:
	-	`sha256:8277176c1ce359800cb1e862f119ef74376d095c67817ac7b18b38749e849abe`  
		Last Modified: Thu, 20 Nov 2025 21:19:42 GMT  
		Size: 11.3 MB (11258063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cdd67ee515764a2f72c402b3167324e44747421ff9c95025025f4ef0ec7b553`  
		Last Modified: Thu, 20 Nov 2025 21:19:43 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b4c766761560cf2785a7bd101f50423b3ccf1d3dbe52ce2f58e656e4cdd2bfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398378525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419184825806ef920f4b70e59370683cf81e4fabab083f24471b5903c9610edc`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:11:21 GMT
ARG version=11.0.29.7-1
# Thu, 20 Nov 2025 20:11:21 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:11:21 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 20 Nov 2025 21:42:04 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:42:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:42:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:42:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:42:05 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:42:05 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:42:05 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 20 Nov 2025 21:42:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 20 Nov 2025 21:43:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:43:10 GMT
USER gradle
# Thu, 20 Nov 2025 21:43:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:43:10 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0f11c98a17ba898a4593e6635646734a5d2e85cfd7c0e876701d59fff75b1c`  
		Last Modified: Thu, 20 Nov 2025 21:20:11 GMT  
		Size: 151.9 MB (151860129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eab54276af3c1651238f514a00d4e899495899939d6421dfcfaa70db8c14b0`  
		Last Modified: Thu, 20 Nov 2025 21:43:02 GMT  
		Size: 85.5 MB (85525613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70f44c72bf6cea29feb5daa16c1033db6fa21289126a1e56e77188e6fb69a0`  
		Last Modified: Thu, 20 Nov 2025 21:42:55 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3111efe9a870c97822ca7cc9f7038ef64856b1cb768004d125282a3dd7524a8b`  
		Last Modified: Thu, 20 Nov 2025 21:44:00 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c3b54376398b6ba7d7060556dc89318ac934eb8ac2f33d64bbf99e14502727`  
		Last Modified: Thu, 20 Nov 2025 21:43:46 GMT  
		Size: 425.0 KB (425022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0fe6a7955eac9088e61a94fe4a2d35fc3f64c320f8374a6cfa3962421ce9b8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633614b461f855a71261b009055817cf8fa39c7a9925325a193a91259623230f`

```dockerfile
```

-	Layers:
	-	`sha256:55a7341fc3e5b8de80ea581d495501de6b711abf1f8d2f33e962c7a4b3c74ac8`  
		Last Modified: Fri, 21 Nov 2025 00:17:35 GMT  
		Size: 11.3 MB (11257882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63ce12a77a5cebcab8455b764652ef845a951724d3f713c9fee33c7de58bfe0`  
		Last Modified: Fri, 21 Nov 2025 00:17:36 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
