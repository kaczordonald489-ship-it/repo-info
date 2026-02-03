## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:cdd92fbf146e46f79402d6b846168308f83a410df1f9eb101e84b1180f468a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9c9118f8d77f55402c5520f9e32d0ca4e3eb213c2bcb92e5afbcebf16239c0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (421957125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb914d0a20dd56095a36fb91c7fa1383b034cc01439e4ab3d94307c55450890`
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
# Wed, 28 Jan 2026 04:56:12 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:56:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:56:12 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:56:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:56:12 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:56:12 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:56:12 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 04:56:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 04:56:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:56:15 GMT
USER gradle
# Wed, 28 Jan 2026 04:56:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:56:15 GMT
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
	-	`sha256:e09948fd9b114da2e8f61fc29d25f80cfca4401c9c79588e9d093624e0efa98a`  
		Last Modified: Wed, 28 Jan 2026 04:56:46 GMT  
		Size: 86.0 MB (86040349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c3df039ff71d1bf780572fb777fbd398c554705e0c9516827924b60d585b53`  
		Last Modified: Wed, 28 Jan 2026 04:56:43 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf0c4442672873627591df5f1b50eb6bd57a4c5249d7b654fb8e31cd99a78c1`  
		Last Modified: Wed, 28 Jan 2026 04:56:47 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee4f96a6299dbe85e0af2a03bc2b2548b7ebdd294b9c7cdbf1e8292b1ca7fe0`  
		Last Modified: Wed, 28 Jan 2026 04:56:43 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:42c6584ad5762294afef65e384fc1f3cde27799049eac101986cf02e6772c246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b339f7d87950a5501d8dd54056cfd5102bf3646dc8358d123ec5b099fccf24e`

```dockerfile
```

-	Layers:
	-	`sha256:ee01454ef869bd65122617bb1e1dd0189f07abea9458abac18434abbc30abaf1`  
		Last Modified: Wed, 28 Jan 2026 04:56:44 GMT  
		Size: 11.3 MB (11275975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd470b2f2cfc89ee4eb1d9e7d70f4a9cd0cbd823ac328a33357af36745ac5a3`  
		Last Modified: Wed, 28 Jan 2026 04:56:43 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d529546bc2effe52b4f1451b4ef7c7d12d38b831161d7047ea7681fbf6b1aed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418880690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f165fde1067005a2ada7f6b941c8d301f8b47219b717d393a26efe59098b70`
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
# Wed, 28 Jan 2026 05:38:14 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:38:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:38:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:38:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:38:15 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:38:15 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:38:15 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 05:38:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 05:38:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:38:17 GMT
USER gradle
# Wed, 28 Jan 2026 05:38:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 05:38:18 GMT
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
	-	`sha256:5d99e36399f3a384506e57aa9852eaf4ba7a5c7bd7edbe1664dff49fcc3c8090`  
		Last Modified: Wed, 28 Jan 2026 05:38:49 GMT  
		Size: 85.5 MB (85511686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b836144ab7000f433412e6768d4753ff302f7f1cdd885a9542b3c2923458554`  
		Last Modified: Wed, 28 Jan 2026 05:38:45 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188dc6989ea75b344d9b08e90d5836de5cd1f74a112391936f49881b615612a9`  
		Last Modified: Wed, 28 Jan 2026 05:38:50 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e57fda2eb9d6d0a5bc4ce8ab8d3ba745e01de4d22333307d0753a2c2b4daf0d`  
		Last Modified: Wed, 28 Jan 2026 05:38:45 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b34d7768cabed7d139a3e53dcdf99e983ded58fe599c9e3cb33c5e500f7086ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb2bedbce7481e3b838a28d9721d320c80dc27e3649213a29b0c1b6c00d9002`

```dockerfile
```

-	Layers:
	-	`sha256:dfbd6454b41f5b4f8477d2a10b2089359dd8364fc2a4c7884c24d9a053953d5b`  
		Last Modified: Wed, 28 Jan 2026 05:38:46 GMT  
		Size: 11.3 MB (11275794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e60d5e72adf331363753960f4c1bfdfde2ab64e4283c28d8d4d64c90ccfd14`  
		Last Modified: Wed, 28 Jan 2026 05:38:45 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
