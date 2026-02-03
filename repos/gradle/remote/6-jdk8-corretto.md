## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:4ee82c0c4526a2be5ed7c1cc966e3409aeb40dea7e94cadb3b64345b3b6e51c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:7ba921141728286ddd961cf0070c7ec5f3c4eac5f037009a783d03245d9231c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.5 MB (558455399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18000337a29d9b611286cbf1fc251ccde52d48777c865efb9fb375dd58ce7155`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:07 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:07:07 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:07:07 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 28 Jan 2026 04:56:19 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:56:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:56:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:56:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:56:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:56:19 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:56:19 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 28 Jan 2026 04:56:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 28 Jan 2026 04:56:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:56:21 GMT
USER gradle
# Wed, 28 Jan 2026 04:56:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:56:22 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be7c2edf409bd473264db3dd583bdea68108cda313a28b0280794e16c7fb62`  
		Last Modified: Wed, 28 Jan 2026 04:08:00 GMT  
		Size: 330.9 MB (330931260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0a99b06fac58db9e50f0f82abf5068f035319b0deb94a464da855ed1408840`  
		Last Modified: Wed, 28 Jan 2026 04:57:04 GMT  
		Size: 65.4 MB (65370381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb629aeeb8499a42b7bea40720c9248b5e70730d320cfe4b719fc38db1df5d2c`  
		Last Modified: Wed, 28 Jan 2026 04:57:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd88491465caa9fbd1ab97c47c71fd4f976b402761d30aeb1847b93386a7490`  
		Last Modified: Wed, 28 Jan 2026 04:57:05 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d2254be5abff45b9747ec3ad96552bf19a7e6e833115eb34459937ed86f8`  
		Last Modified: Wed, 28 Jan 2026 04:57:01 GMT  
		Size: 431.3 KB (431283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f65035af3290ee9136ae68b5a48b67f16e2d5c4fafdf27ff6d9cd7303aafc09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18066825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a05cfef4acd39dd2bcabfc6a1b815e8c8f0bf1fc7e7420e4ba6b1d48973681`

```dockerfile
```

-	Layers:
	-	`sha256:ddc4473e45c2d5d387ddf10572b4a9fa9a08f24032070cce1fd5a04f3e1032e2`  
		Last Modified: Wed, 28 Jan 2026 04:57:02 GMT  
		Size: 18.0 MB (18045960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80084c5362cbba5540922ad55642e8eddc8f51267131de40da408e0216fcc797`  
		Last Modified: Wed, 28 Jan 2026 04:57:01 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:62202b151b73648cff6f3c05c9742741cf8fd919161d262e48b6c85b178e6f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364508614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1be5d72cc3749b3cf513e9914f10eb3bb93fe3882f895185d2d92c896e6460`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:26:51 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:26:51 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:26:51 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:26:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 28 Jan 2026 05:39:03 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:39:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:39:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:39:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:39:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:39:03 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:39:03 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 28 Jan 2026 05:39:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 28 Jan 2026 05:39:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:39:05 GMT
USER gradle
# Wed, 28 Jan 2026 05:39:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 05:39:05 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b45e58514dc885fb56c900fdbc7ed10c585684bf1073c2a46548f3f3d57774f`  
		Last Modified: Wed, 28 Jan 2026 04:27:11 GMT  
		Size: 118.0 MB (117962435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e10b3b63a05494344bb84461825f52c19802f4728e7e3d1e43f2f12ed5a9b`  
		Last Modified: Wed, 28 Jan 2026 05:39:35 GMT  
		Size: 85.5 MB (85506180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c144c92a31ce711570659c17063db6919d78b9059450938f95761118f81f512`  
		Last Modified: Wed, 28 Jan 2026 05:39:32 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211fd2f59b5bf9a7935173c97203641c97fcd46fe8f281716e72457af12728f5`  
		Last Modified: Wed, 28 Jan 2026 05:39:36 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a97e16809a0b33102d4c559718d79332fdf81a5deeb750304a33a4d24e55b9`  
		Last Modified: Wed, 28 Jan 2026 05:39:32 GMT  
		Size: 425.0 KB (425020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:ce67d7b5b73579f43eebd5cc8e37cc23d32cfd35bb5cb216051830d578a1b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11631162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce4a7068cebcfb5f7b43196c0301713b3fc9a8de6bf848d22a3f632ad6cf6a8`

```dockerfile
```

-	Layers:
	-	`sha256:051fcd2f5276e088046b804871979b02f7bc29d7f776ec87fd6a93164efb7789`  
		Last Modified: Wed, 28 Jan 2026 05:39:33 GMT  
		Size: 11.6 MB (11610124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995f9097d2ae43754180e6fba4d663d6b9515c08ebeb3b7c387c042a029239f3`  
		Last Modified: Wed, 28 Jan 2026 05:39:32 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
