## `gradle:9-jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:b9f96018788b51be9ae8ea98ac31b04fd557c4f7f852dd3dc9f8020d2591621e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:60cb92ba77fa0edd1374108624d06c610d76c019a6c550ad3dccbd809505df70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464710595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9653578fcc1267bea8b8ba7335010282d6293cdb3f7f482a270c4d172c4e27ff`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:39:22 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:39:22 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:13:27 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:13:27 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:13:27 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:13:27 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:35:09 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:35:09 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:35:09 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:35:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:35:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:35:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 20 Nov 2025 21:35:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:35:10 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:35:10 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 20 Nov 2025 21:35:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 20 Nov 2025 21:35:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:35:12 GMT
USER gradle
# Thu, 20 Nov 2025 21:35:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 20 Nov 2025 21:35:13 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73615f162427717bb524bb65d17f76492dd2ba484b36570400ed1948c74aa5ed`  
		Last Modified: Thu, 20 Nov 2025 21:34:24 GMT  
		Size: 189.1 MB (189136491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd08877023c6ad21b5546987c101cc15229360c73b1cf2139f647cd5013661`  
		Last Modified: Thu, 20 Nov 2025 21:36:08 GMT  
		Size: 86.0 MB (86026342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eef87ae8f853bfcdb9acbb29062554214daf2a65b3c0b926b6393b4446a311`  
		Last Modified: Thu, 20 Nov 2025 21:35:59 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01347016cb1baef9b0328fd3eea5d833471cc91eee86e2f6c169a1ad676f9b5a`  
		Last Modified: Thu, 20 Nov 2025 21:42:24 GMT  
		Size: 135.5 MB (135522053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb771b199fdf2a13e2010ec097aae19261312ae704e7ed1d9b07c35fd532b73`  
		Last Modified: Thu, 20 Nov 2025 21:35:59 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4fd00d315a98ad696e23767d76a6e6fd0d1bb1cbffb11a140216adb26fb181c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11378151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abad99e895f4debdd445593b934e4e8e5f23a382531e1d6e52d42dc2804322ad`

```dockerfile
```

-	Layers:
	-	`sha256:54d45a810ac37fcd4aae76fa5770de9ea21ed93ab6bbf8b7e97827df5c298b6b`  
		Last Modified: Fri, 21 Nov 2025 00:22:37 GMT  
		Size: 11.4 MB (11351675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703c0ee5033b70981141e2f05e098d0ae81a200cfa11c4ed644986ffde838589`  
		Last Modified: Fri, 21 Nov 2025 00:22:38 GMT  
		Size: 26.5 KB (26476 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b5b1665ad4dd0a0b59f74e04266cc830817216c32c2ac6aae5974d3e5e3a9c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461037078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b788a85e01666797e56fc726bdd8d513f174779103160d4a85c1acb595c75b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Nov 2025 19:38:54 GMT
COPY /rootfs/ / # buildkit
# Thu, 20 Nov 2025 19:38:54 GMT
CMD ["/bin/bash"]
# Thu, 20 Nov 2025 20:16:56 GMT
ARG version=25.0.1.9-1
# Thu, 20 Nov 2025 20:16:56 GMT
ARG package_version=1
# Thu, 20 Nov 2025 20:16:56 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 20 Nov 2025 20:16:56 GMT
ENV LANG=C.UTF-8
# Thu, 20 Nov 2025 20:16:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:40:14 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:40:14 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 20 Nov 2025 21:40:14 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:40:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:40:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:40:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 20 Nov 2025 21:40:14 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:40:14 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:40:14 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 20 Nov 2025 21:40:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 20 Nov 2025 21:40:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:40:17 GMT
USER gradle
# Thu, 20 Nov 2025 21:40:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 20 Nov 2025 21:40:18 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89032ad19d026518bda7c21ccdf4d5da20cfd0f783042990bddb410e19dc6d4d`  
		Last Modified: Thu, 20 Nov 2025 20:23:40 GMT  
		Size: 187.1 MB (187059620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0ccbc7f7d30c02551e655f98462904775e2e89dcdd646581146c46a88dbdf4`  
		Last Modified: Thu, 20 Nov 2025 21:41:14 GMT  
		Size: 85.5 MB (85524733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884bb7301c74e574e1cdf38b976afa1b6b2d841554f8a9be6395960b398bdbc`  
		Last Modified: Thu, 20 Nov 2025 21:41:04 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea977da957a0e0170d4784a579845d2485b94108879bcdd25accb01c92b0f36`  
		Last Modified: Thu, 20 Nov 2025 21:44:30 GMT  
		Size: 135.5 MB (135521969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66930c893fc400224dc0384141f7b6a2d4e879680a66a2625d79597b3f2a38`  
		Last Modified: Thu, 20 Nov 2025 21:41:04 GMT  
		Size: 59.5 KB (59548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:22dd8040401514575cf574bdacf9d789ca85e6464d9616622157fc887f7e46ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11377554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631da7e40c94250e6715a6bdea0e2c9454744b3bd63aaf7b5cd97056ed85928e`

```dockerfile
```

-	Layers:
	-	`sha256:59a4da9c1b2ae3664e55babe3d11ac4164b53671f7dc7322b62f8c9cf9c368c2`  
		Last Modified: Fri, 21 Nov 2025 00:22:48 GMT  
		Size: 11.4 MB (11350784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e6c21d4608e43135ea32749f6003fa8106adb9837423917e8d958441fd4518`  
		Last Modified: Fri, 21 Nov 2025 00:22:49 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
