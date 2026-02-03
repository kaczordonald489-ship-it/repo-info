## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:982d0834f8476bb7d1f44e1dae0edde4badb55c5bf57e251fe597f55ad819e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:94d5961e6a641c6fd81ee6ff77e650bf972f82a96a603919c9ca3c0b6c346e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425499797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd756ab370f166da563c9d97d56da761ba8f480129133931bd81eb89ebd3721`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:21 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:21 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:21 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:21 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:11:45 GMT
CMD ["gradle"]
# Thu, 29 Jan 2026 22:11:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 Jan 2026 22:11:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 Jan 2026 22:11:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 Jan 2026 22:11:45 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 Jan 2026 22:11:45 GMT
WORKDIR /home/gradle
# Thu, 29 Jan 2026 22:11:45 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 29 Jan 2026 22:11:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 29 Jan 2026 22:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 Jan 2026 22:11:48 GMT
USER gradle
# Thu, 29 Jan 2026 22:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 Jan 2026 22:11:48 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bcfb83c2e453e939721a922013646100eb7e7c7d5c82e4ecd27e63620b69bd`  
		Last Modified: Thu, 29 Jan 2026 21:32:47 GMT  
		Size: 156.9 MB (156915770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5401674a207a278670d4c3313be414d8d2399640e04a880c46910bc060ef15f`  
		Last Modified: Thu, 29 Jan 2026 22:12:18 GMT  
		Size: 86.0 MB (86034212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b69733d97f79ba65d4d0cb5c52bac4603865201e6983498dd50c8650cb5bee`  
		Last Modified: Thu, 29 Jan 2026 22:12:14 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4db86c539ba27081b6e0b3697d5b2e044662b3bc52e541ade89a50a5f1607`  
		Last Modified: Thu, 29 Jan 2026 22:12:19 GMT  
		Size: 128.5 MB (128469407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1151ad3269f6b8aa6a38d4f49237e2e8aa725f73923d6ec836a51c58be924f`  
		Last Modified: Thu, 29 Jan 2026 22:12:15 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0c1759740ec3116383a36eb3fdafa78a91ded862136fe4f23cfe4318a33e6d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ca22cdb60bb0f97107f8d7c3326e8618678b1f252c0fcdbdbf164486b671bc`

```dockerfile
```

-	Layers:
	-	`sha256:ede9cda0bd2b6ac73c08611911b18b5ccd99044cb69f6076f1172b6d76602f65`  
		Last Modified: Thu, 29 Jan 2026 22:12:15 GMT  
		Size: 11.3 MB (11250465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328bd168611e36673be556b6690f535e09b0c13a0cef917b5cd8b6a3856abd43`  
		Last Modified: Thu, 29 Jan 2026 22:12:14 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:152ce63e83018101c19ae16a82aa8b6630ef3243d78e9be9867f39cb96609e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422691981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adae17696dec39879e7ed313095918c56d7cfb01a2e01a5cebbd101cd9d1d6e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:32:24 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:32:24 GMT
ARG package_version=1
# Thu, 29 Jan 2026 21:32:24 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 29 Jan 2026 21:32:24 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:12:02 GMT
CMD ["gradle"]
# Thu, 29 Jan 2026 22:12:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 Jan 2026 22:12:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 Jan 2026 22:12:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 Jan 2026 22:12:02 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 Jan 2026 22:12:02 GMT
WORKDIR /home/gradle
# Thu, 29 Jan 2026 22:12:02 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 29 Jan 2026 22:12:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 29 Jan 2026 22:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 Jan 2026 22:12:04 GMT
USER gradle
# Thu, 29 Jan 2026 22:12:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 Jan 2026 22:12:05 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065d21b4470e9f024846f039ffce24548a54e0966b2b32586c3e1d734b91367b`  
		Last Modified: Thu, 29 Jan 2026 21:32:49 GMT  
		Size: 155.7 MB (155728159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5367870301331174cf4db224fd122d7d0b1dcfc409c68c674526c99b21890f7`  
		Last Modified: Thu, 29 Jan 2026 22:12:36 GMT  
		Size: 85.5 MB (85516565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7036c02bb3c1140ec51f414306f0f813f53d9849436de5c3a4486dbbcbf97cf2`  
		Last Modified: Thu, 29 Jan 2026 22:12:33 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be694d4b60842d94a69a34e45e40ffb446125c65c251d03a96b598ee2ea969d`  
		Last Modified: Thu, 29 Jan 2026 22:12:37 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa71bdd8211954b7171db14eb2ee6d8a132e81c408b08c5ab78db46f97b8deee`  
		Last Modified: Thu, 29 Jan 2026 22:12:33 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:317026a9b95935feb62a874945b0cc58ae7fb8c8c9fa1077f1b30805f4efbf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96b564ed8dc19b62eb59998edc769207755572ff2001df5e3216e60eb21ed41`

```dockerfile
```

-	Layers:
	-	`sha256:b897c8ed351326bc1f8c477df236468a7f1ff91f56e766379fab5fc163c8ebd9`  
		Last Modified: Thu, 29 Jan 2026 22:12:33 GMT  
		Size: 11.2 MB (11249440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a24609b13d5812026b0ddf826f9a3745f5394556a5d4c1143d7bdf53f2be6c`  
		Last Modified: Thu, 29 Jan 2026 22:12:33 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
