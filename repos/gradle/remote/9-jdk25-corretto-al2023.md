## `gradle:9-jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:6c9f79e1c164b64ca0ca7f6f641975d77610cc5ca3e6e905f65ab8c16c6866cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:bf7743ea08981941da4119cbd296e86c34016c443efa4b4dde345cb841a5e43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466297284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfbb5d6c3f6b8f6a199fd262b91b0efd1e36201f9731667bd63df0ba3bc9347`
-	Default Command: `["gradle"]`

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
# Fri, 30 Jan 2026 17:44:10 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:44:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:44:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:44:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:44:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:44:10 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:44:10 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:44:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:44:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:44:13 GMT
USER gradle
# Fri, 30 Jan 2026 17:44:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:44:13 GMT
USER root
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
	-	`sha256:4f14242a6b8a9fcbe686f31fb89edb438a7be2ce2b72521690062ba0332bed89`  
		Last Modified: Fri, 30 Jan 2026 17:44:44 GMT  
		Size: 86.0 MB (86035436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa232246cf70dcbbb1a6c386479a5751d3d6378ac964110d8559cf15eea83e3`  
		Last Modified: Fri, 30 Jan 2026 17:44:40 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b162c4810c26e965a05eb7b248d16d63ed734f529034e03efcaa752d318b5d`  
		Last Modified: Fri, 30 Jan 2026 17:44:45 GMT  
		Size: 137.0 MB (137019695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b5adf831768a8b28384e30caa02976f614e1b30b420810cc0854a0c0d1e565`  
		Last Modified: Fri, 30 Jan 2026 17:44:40 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5e03c9556ed17679786a892098b5110b8457f10497c8f1d6fdfec219a2908795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5fd27d6ccb9ac69e8de64e95e5bda5c2d2f3bd74751927565ddbbc218688ee`

```dockerfile
```

-	Layers:
	-	`sha256:1e50f3cf42084d063fcc382e97fdd55e4d387a5c0f4f19851a17bcf550343e86`  
		Last Modified: Fri, 30 Jan 2026 17:44:41 GMT  
		Size: 11.3 MB (11338311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daecd320f408c0d7ec9fdb533c53bc4d8ddb32053ef934e8734bd06e715e8c37`  
		Last Modified: Fri, 30 Jan 2026 17:44:40 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ad90db4f6e75800501868d3486da666912c4640f75b397d231211d867c1a6fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.6 MB (462572237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727f2d97956b6737766a2c35fd0026fa2aea6c5527c6bfaea3c9dce9d78196a8`
-	Default Command: `["gradle"]`

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
# Fri, 30 Jan 2026 17:43:29 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:43:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:43:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:43:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:43:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:43:29 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:43:29 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:43:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:43:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:43:32 GMT
USER gradle
# Fri, 30 Jan 2026 17:43:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:43:32 GMT
USER root
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
	-	`sha256:6d4371f72c2e5d0da03856e479e7f5c9d1448c105aad472f5e8969ec799143c4`  
		Last Modified: Fri, 30 Jan 2026 17:44:04 GMT  
		Size: 85.5 MB (85514027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d56afee1c22cd7436aa6e0516150db960e50a145ba72b5f4e681a35a784f41`  
		Last Modified: Fri, 30 Jan 2026 17:44:00 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0068106a5a62292487f481f06866f2f75d9563d0632b4fc429f39da4dee54f2`  
		Last Modified: Fri, 30 Jan 2026 17:44:05 GMT  
		Size: 137.0 MB (137019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1385e98aa64fdad4ffd08a785dd0474e17439de19226e2d2c778bbfcfa23a4`  
		Last Modified: Fri, 30 Jan 2026 17:44:00 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:36b51a5c1f6b0ae4df5e42f7f840cdaddd56e7cfa85abbfe8a7698c82bc0e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d297d96a843e6493c5f54fa3bd24727ac6999df68cbea5e15634226e0ac719`

```dockerfile
```

-	Layers:
	-	`sha256:c2a810c8316e09d0aff3028527a446aa88f97798ff099e8adc44bc24b52831a2`  
		Last Modified: Fri, 30 Jan 2026 17:44:01 GMT  
		Size: 11.3 MB (11337348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61d5a9a5c25540c952bae9576a72c6350352a6316177e53e52be6b92fb99de3`  
		Last Modified: Fri, 30 Jan 2026 17:44:00 GMT  
		Size: 22.5 KB (22489 bytes)  
		MIME: application/vnd.in-toto+json
