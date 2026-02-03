## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:322da645e9fb1fe18d67c0876ef80716b098e9d68b8508d0764229182cbaf79f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:90075c855422218efeaf9593cfab599bbe7a17a2ed25371e6c8f4288099af32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578851693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3a86b863276683b0a26c4b543a17a511966393ad313e4a34db5422b54ae23d`
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
# Wed, 28 Jan 2026 04:56:14 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:56:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:56:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:56:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:56:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:56:14 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:56:14 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 04:56:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 04:56:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:56:16 GMT
USER gradle
# Wed, 28 Jan 2026 04:56:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:56:17 GMT
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
	-	`sha256:598a2366a3c2e6d3aeb3442de4574131988fbeb5efa15785ed7be0e02f20be6e`  
		Last Modified: Wed, 28 Jan 2026 04:56:55 GMT  
		Size: 65.4 MB (65370294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80606d4a6b7fbd24b2eb6454487147fe83e29caf3f9b4f7f38a10b233cda9`  
		Last Modified: Wed, 28 Jan 2026 04:56:52 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbcc1f6cf44daf58e64533d27b307eb6210d8e6591e99dff02d44a656bcaff0`  
		Last Modified: Wed, 28 Jan 2026 04:56:56 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3a6c698f52337585775678a5e6cf277351ea1851589866e00d4d6d8dc7def`  
		Last Modified: Wed, 28 Jan 2026 04:56:52 GMT  
		Size: 54.9 KB (54911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d6d9eca223c1eaeaa94eecfe2f59e32119dd184f376d8df6128bdf83c6cf005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d64605615b4b7bb165550d930b9079177118a0a7798c6ddc15b7d43b3c51d5`

```dockerfile
```

-	Layers:
	-	`sha256:806ea5bbc187923dee6386159945db1910be721fc28a64d63718f496d1c8bfb8`  
		Last Modified: Wed, 28 Jan 2026 04:56:53 GMT  
		Size: 18.1 MB (18063856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a78c6919bc47cc4c0e158904fd0f49060627b62952e349825f015a9f1316814f`  
		Last Modified: Wed, 28 Jan 2026 04:56:52 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:be40e07931f896787d40ac2910030fdba370d889f5b96695e41dd2d202f96aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384916118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c072856ae002e81db6a717493bcd79aed8f31b6ed23eca95d36f90cd787a8f2f`
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
# Wed, 28 Jan 2026 05:39:08 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:39:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:39:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:39:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:39:08 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:39:08 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:39:08 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 05:39:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 05:39:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:39:11 GMT
USER gradle
# Wed, 28 Jan 2026 05:39:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 05:39:12 GMT
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
	-	`sha256:33ea6bff9ee7a4e75042278be8ac0d25d0c11845dff524dcef58102bf96963e0`  
		Last Modified: Wed, 28 Jan 2026 05:39:43 GMT  
		Size: 85.5 MB (85506420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c525d66c9d7719bf403f1d3acf731b35230cd93a161026c9d9d3ddcd4e80a6d`  
		Last Modified: Wed, 28 Jan 2026 05:39:40 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63f06ecdb87812dcebbad071c354579582373cae1b3d55663f521e4c7baf12e`  
		Last Modified: Wed, 28 Jan 2026 05:39:44 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fbee671bd5da5dfa4abbc93cbcb7b2a05682909ca29db2b23bb57c97b80ef1`  
		Last Modified: Wed, 28 Jan 2026 05:39:40 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8fce5ce3719f2e06e094dfda40c4deac2cb72f4318407581d6894fc9802c0c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11649060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6d9733220fea46bf34d78ef98b39c850cf00d972162b7e6d01fd28ddd5ddb5`

```dockerfile
```

-	Layers:
	-	`sha256:92cb1f5464bdb7ec96d9180109e86a5db9582933a57f732043e686e55deed39b`  
		Last Modified: Wed, 28 Jan 2026 05:39:41 GMT  
		Size: 11.6 MB (11628024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6833080f6e91e79c15c67fb478dbb1dca8ecb19d437a1cda8408f1a4522499d3`  
		Last Modified: Wed, 28 Jan 2026 05:39:40 GMT  
		Size: 21.0 KB (21036 bytes)  
		MIME: application/vnd.in-toto+json
