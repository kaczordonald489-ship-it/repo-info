## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:48863bf4cc4efa49112fc57cf16b47a1f4f22c33bc66b6b3b9a5a9b0b87f3ddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:887172c3732278e611dd7b8d244ef2990f217bb29ae69340fd755e1abe12cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.8 MB (421832020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df95ecc0774eb2268ea99019392f8410143e30ea18f0ebc7d3b6b6821e92e1`
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
# Thu, 20 Nov 2025 20:48:09 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 20:48:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 20:48:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 20:48:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 20:48:09 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 20:48:09 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 20:48:09 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 20 Nov 2025 20:48:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 20 Nov 2025 20:48:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 20:48:11 GMT
USER gradle
# Thu, 20 Nov 2025 20:48:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 20:48:12 GMT
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
	-	`sha256:eb8b1180ea76789de51610349d7ea735794b00e2b3a74897f7b9eac5212006a2`  
		Last Modified: Fri, 21 Nov 2025 00:34:50 GMT  
		Size: 86.0 MB (86023923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9558a477f5635d532d1fe0968362308f6903abb7530760ec9bd892d8c1a61a6d`  
		Last Modified: Thu, 20 Nov 2025 21:32:46 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b599e840deada22b1c2a3fe1c266911460763f813fb5044a2e05993d07d18`  
		Last Modified: Fri, 21 Nov 2025 00:34:55 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca03285702948470c693a302846ca60f1a718026a419cffd16202ab1e0bef7d3`  
		Last Modified: Thu, 20 Nov 2025 21:32:46 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b512c9186a4eb940203cb257f687ad69c17e27f044d684b9e3339014d92bd6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3860f6940ac2abaa6e0ee133d130ae6519fc66979641ba7b18d7af75259ca0`

```dockerfile
```

-	Layers:
	-	`sha256:1d6b8d405ffb0d60babd569ec7089da241afc40c4e76eb848e3dbbed09274b2d`  
		Last Modified: Thu, 20 Nov 2025 21:20:25 GMT  
		Size: 11.3 MB (11275963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bfe55091f2633a48f04f10f842a88162c86a2d93fba6a460d98f230df4c1025`  
		Last Modified: Thu, 20 Nov 2025 21:20:26 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7bde609705effd5063ddb3566254a814b747b21d5fd1b918cbc9702490580d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.8 MB (418785540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6164d74b246faa399543d851a63074904d24c028b5909e3d46b1930b70e9772a`
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
# Thu, 20 Nov 2025 21:43:00 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:43:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:43:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:43:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:43:00 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:43:00 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:43:00 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 20 Nov 2025 21:43:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 20 Nov 2025 21:43:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:43:03 GMT
USER gradle
# Thu, 20 Nov 2025 21:43:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:43:04 GMT
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
	-	`sha256:6a9bf7d25afee751f63e4d04189ee43b2ce902a3699058038f2fed93c4d89c92`  
		Last Modified: Thu, 20 Nov 2025 21:43:59 GMT  
		Size: 85.5 MB (85525387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a19b8f1c9be124383644822f9d4f8dfb6bcfd75739d569c1625dd20ad7b07fd`  
		Last Modified: Thu, 20 Nov 2025 21:43:47 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c56f7df277744b78683e6da1a536699fa3c2612c490e1da5e4848bc7d5bc67`  
		Last Modified: Fri, 21 Nov 2025 06:07:52 GMT  
		Size: 128.5 MB (128469408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f3ffda280820086a0c9a9dea33def638a609d3bcef592b777e7ad70de3ad9b`  
		Last Modified: Thu, 20 Nov 2025 21:43:47 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9f7e9aa694feaf5be3526cb8f02704d5b0451d0b9819af57efc39fdfaeab86bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9bc87b63e2f5f8c31099ad5991658fae698c0570eb0cfc73acb662a17bc3f5`

```dockerfile
```

-	Layers:
	-	`sha256:deb95a198a2c2c70f96f3636f02598829ee2c2ff59bf00c8fc38b4b62c095c7d`  
		Last Modified: Fri, 21 Nov 2025 00:18:36 GMT  
		Size: 11.3 MB (11275778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9199a3a073af6ad97bb4e0bbe17db4e820be9cadf13b1babe8d07cc544a6a80`  
		Last Modified: Fri, 21 Nov 2025 00:18:37 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
