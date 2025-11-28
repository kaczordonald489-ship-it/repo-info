## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:b1ddb640ab40bb7e0e6a91ccf82082864a50349eb579b126d607faec9cc96ed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:89775eef3b3383abf09463f8b50bfd78b46a5deebd562bf58adae88c3db960ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464710382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c86cacdf971cb816d509db72ac4cd0412d7660326f822943a73ba685396fd9d`
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
# Thu, 20 Nov 2025 21:34:48 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:34:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:34:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:34:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:34:49 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:34:49 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:34:49 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 20 Nov 2025 21:34:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 20 Nov 2025 21:34:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:34:51 GMT
USER gradle
# Thu, 20 Nov 2025 21:34:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 20 Nov 2025 21:34:52 GMT
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
	-	`sha256:e98106c24f22bb5357e6c6dc569e367fcfca11b85922c9ac2e93b8882db4336b`  
		Last Modified: Thu, 20 Nov 2025 21:35:54 GMT  
		Size: 86.0 MB (86026319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf13c88ca4d560d8865c6167e00f0e1ed1bf0fd29d6287e785979b3b34a86711`  
		Last Modified: Thu, 20 Nov 2025 21:35:45 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6e4d7dc645e01d00afe6ed945ff074fc31bf9f71e761cbe2dd2aea7e3f04c8`  
		Last Modified: Thu, 20 Nov 2025 22:22:23 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679146191cd61def9176ece2add002c5c2501649c1f0bf5e8689b712810a9d0`  
		Last Modified: Thu, 20 Nov 2025 21:35:45 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e743ac8be19dd2ea6210497095e2e4673bb76f9626f62f99fb62a3903d9c56f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e2ccd9606dcebc13a3b23c3c47e629389efe3feab1df0cc97be7b9a7c4492`

```dockerfile
```

-	Layers:
	-	`sha256:984e01aa9edc758e3e71eee747d95fd3202e6a4363df4ffa05a4bb1353dae3cf`  
		Last Modified: Fri, 21 Nov 2025 00:23:34 GMT  
		Size: 11.3 MB (11349325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6242cff4a0e6b93d9d70acb882f3b7c777dafd61ffee63fd8c8bf2cdc7c1de1`  
		Last Modified: Fri, 21 Nov 2025 00:23:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e23f3b85a8925053c74671e3030ee7e161978a4207fefaf41930d9bfa525fcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461036610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f49d799ee1ec583886fbf0fac63809e9be23371f69abcb29fcea9bdddc6dc3a`
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
# Thu, 20 Nov 2025 21:38:27 GMT
CMD ["gradle"]
# Thu, 20 Nov 2025 21:38:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 20 Nov 2025 21:38:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 20 Nov 2025 21:38:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 20 Nov 2025 21:38:27 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 20 Nov 2025 21:38:27 GMT
WORKDIR /home/gradle
# Thu, 20 Nov 2025 21:38:27 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 20 Nov 2025 21:38:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 20 Nov 2025 21:38:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 20 Nov 2025 21:38:31 GMT
USER gradle
# Thu, 20 Nov 2025 21:38:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 20 Nov 2025 21:38:31 GMT
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
	-	`sha256:c6f7946dd29f3a813ec2cb4ee852a9b20186a986b83a02c28c56084ed963fac0`  
		Last Modified: Thu, 20 Nov 2025 21:39:42 GMT  
		Size: 85.5 MB (85524393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d6cc80ba44dd245b7f06f1f930f3d5a9b287a23005d7c890a6876139dbe5b8`  
		Last Modified: Thu, 20 Nov 2025 21:39:26 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9574b8dd325c3814c6c6d451424d8a765e0529df84fed0ae20e1a391b2c770f`  
		Last Modified: Fri, 21 Nov 2025 06:45:28 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c56182aaeec640795d5fc8f41b382a44622e5bda8a9f47240331a78a80326`  
		Last Modified: Thu, 20 Nov 2025 21:39:27 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:958a90936b916053ac9386f8c0391c472b321cf6e5fef6c1f1c1d7970f0a9f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00abc5182038e968f5a1d10e760aa5e910d58b7eb96eab258c6c9670ba1c6e2`

```dockerfile
```

-	Layers:
	-	`sha256:3866981e6cb3f5b115fc8ba484447193704a458b2069587dc2b2b76793da048d`  
		Last Modified: Fri, 21 Nov 2025 00:23:45 GMT  
		Size: 11.3 MB (11348362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad86bad91e69b266410a1654411b903d4adae442fb5c4608d1eb2b071f7bb4c1`  
		Last Modified: Fri, 21 Nov 2025 00:23:46 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
