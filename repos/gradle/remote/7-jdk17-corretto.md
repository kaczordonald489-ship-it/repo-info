## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:7611d8074c5b9bd5f8e45f7abe083732937ebef93fb1d1a2b6d478cd66161c82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6c6dcf4230f85e1795ec90193807f6cef1c0b6747664b8957002ab8a89732360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.4 MB (425408622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da865aeb9a63e7a8d23ee182f678bfa5a738db39e5fca368454145651d3a4d7b`
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
# Thu, 20 Nov 2025 21:36:14 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:36:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:36:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:36:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:36:14 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:36:14 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:36:14 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 20 Nov 2025 21:36:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 20 Nov 2025 21:36:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:36:17 GMT
USER gradle
# Thu, 20 Nov 2025 21:36:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:36:17 GMT
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
	-	`sha256:7ad27d3a2ced690c76b4e339e89bc34c144515eb3ee8c44e98ef10693f940151`  
		Last Modified: Thu, 20 Nov 2025 21:37:03 GMT  
		Size: 86.0 MB (86015189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37725e9d5f0c30fd8ee93066fbbe9754addd5b5e520542778ab0eb1087ce7619`  
		Last Modified: Thu, 20 Nov 2025 21:36:53 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361bc765dcbe890a8ee1d740e5ac0503578ff9fd4b25c5d22a196ddc12a4a21`  
		Last Modified: Fri, 21 Nov 2025 00:20:41 GMT  
		Size: 128.5 MB (128469439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181314ced3796f5adf609edf981158c90bf48f76e19091ea5913e58513a5bb4`  
		Last Modified: Thu, 20 Nov 2025 21:36:54 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:ae679a38a8a25063ff1a285a9ef1efd57869fe5878054e7e5af1f647fe065b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00be1189046faa4b343a66b61c1782ba8fed1cfa9e32724dc04ab433a95c542d`

```dockerfile
```

-	Layers:
	-	`sha256:22081653005571a7a5c7d380fcc66ec593f9fcb06db7faa6b7bae0b3399e4f10`  
		Last Modified: Fri, 21 Nov 2025 00:18:45 GMT  
		Size: 11.3 MB (11250463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f963102f4aefc68fc831d79bcd26910e3a7ae89170e03e9680b4f468f8e36f6`  
		Last Modified: Fri, 21 Nov 2025 00:18:45 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6d25c88bb2e0b1394d10f904c74a8a38ba92037c22b4b5afa764bb59fad9b166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422634141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f65a0f0baf5f868d471b41cc49fc788f66217b7e5911187c8e8a510c7686f`
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
# Thu, 20 Nov 2025 21:42:18 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:42:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:42:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:42:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:42:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:42:18 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:42:18 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 20 Nov 2025 21:42:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 20 Nov 2025 21:42:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:42:21 GMT
USER gradle
# Thu, 20 Nov 2025 21:42:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 20 Nov 2025 21:42:21 GMT
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
	-	`sha256:7d3e0b1a556726686b15b6baa3ce6efee3120760b41cbf964acd9cd7bb6fcdf2`  
		Last Modified: Thu, 20 Nov 2025 21:43:22 GMT  
		Size: 85.5 MB (85525894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0af2ebd9eae723100870708c79b895708507c5221cce7036536e4f8c56fc4db`  
		Last Modified: Thu, 20 Nov 2025 21:43:15 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378d4ece468344177efdae740cf5574ab46ce6eeeb39fb5f5acb1d5ff595707`  
		Last Modified: Fri, 21 Nov 2025 06:09:31 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1327495d3de9bbbffa649ecbe6f06b4c6f62662a7dd0ecfa1b1aabe895881520`  
		Last Modified: Thu, 20 Nov 2025 21:43:16 GMT  
		Size: 59.5 KB (59516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8f8eb21722648274fbf788e8d6202c948c7a164f45f3fcafe03076de99e14f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d469180882d326ff90a1df1c39ffe186afe39feb5cae0632b961024189e30c8b`

```dockerfile
```

-	Layers:
	-	`sha256:fddb0e976dd09b113c494c62c547dafb65b8ce8a5a7b8a8cdeaaa1ef8a6e8237`  
		Last Modified: Fri, 21 Nov 2025 00:19:03 GMT  
		Size: 11.2 MB (11249438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db930ae2ad403ba3630b9340b517028f23c1512ed3d76d00403d7e2fd1d125ff`  
		Last Modified: Fri, 21 Nov 2025 00:19:04 GMT  
		Size: 20.9 KB (20885 bytes)  
		MIME: application/vnd.in-toto+json
