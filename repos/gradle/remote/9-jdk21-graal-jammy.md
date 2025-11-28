## `gradle:9-jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:ba40786a6d946bd35457017d8d6d786bd2db585ea037b6e7a6aed9feb861296e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:c12bde9e8e19d5ccb447b2ed0c3a31e5ba8ce658e5b7d9a0cee301edd20f9d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.6 MB (581644050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67148d26d4366eaaf65c7a461219a55c296d3eb1b5e72a390faec6ebe87cfd9f`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:59:23 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:59:23 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:23 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:59:53 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:59:53 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 19:59:53 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 17 Nov 2025 20:00:02 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 20:00:02 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 20:00:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 20:00:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 20:00:05 GMT
USER gradle
# Mon, 17 Nov 2025 20:00:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 20:00:06 GMT
USER root
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12b3e69a672a28226c1d441506fbbe5c2305656a55ca88a9feafe1c14632d2`  
		Last Modified: Mon, 17 Nov 2025 20:01:09 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21cd8fd0fa50cd56e080dcad94b6da4bc8c22ecd735366be04883bd5e66f844`  
		Last Modified: Mon, 17 Nov 2025 20:01:36 GMT  
		Size: 126.5 MB (126539082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5cb881893e12d2bbf0aae97806d703048e24d163033af935c7dbf7f1e954b8`  
		Last Modified: Mon, 17 Nov 2025 23:39:48 GMT  
		Size: 290.0 MB (289986938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59cbdb10f8380106dd633576ff9a9019c452f84ef3ea8069f3a6a2db39049b2`  
		Last Modified: Mon, 17 Nov 2025 23:41:03 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf897ce5852ae1bcd01fa34512552764474e33e7073431985ceb622600b1bb`  
		Last Modified: Mon, 17 Nov 2025 20:01:09 GMT  
		Size: 54.9 KB (54920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:52d863cfceb4b173b74eca337b3c6d74beae01498149e256f255cef21b343070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9407265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eacb462b038121f20d19ece5c81c16c6c7a85e9310aa8f7723ceed682090951`

```dockerfile
```

-	Layers:
	-	`sha256:71a29d23b01ab352c760e36eff3ee58ec50a23c7a0a1275729034d71e51b51bb`  
		Last Modified: Mon, 17 Nov 2025 21:21:01 GMT  
		Size: 9.4 MB (9377264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccb1316078c19da17a80cef1258ba3740a7d1606f6ffa7626d4cc5a4afe9b201`  
		Last Modified: Mon, 17 Nov 2025 21:21:02 GMT  
		Size: 30.0 KB (30001 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b3873ace256cb169928c6e41679bfe7bb85d8998421ec5f4fef2040c22031f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.3 MB (567270896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5817fd42f7b0e2bdbf84fa5f8389a2e45aeee3989c00ebb2bc61eb138365158e`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:58:57 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:57 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:59:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:59:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 19:59:28 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 17 Nov 2025 19:59:37 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 19:59:37 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:59:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:59:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:59:40 GMT
USER gradle
# Mon, 17 Nov 2025 19:59:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:59:40 GMT
USER root
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c8a15af3cc96a3ad00ea4d2edab7b5cb07a288f0b2282793a33b6591674890`  
		Last Modified: Mon, 17 Nov 2025 20:00:30 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130f97f6331de2d16377b0c71e3d53707a69f0da9013fe94ae1f3b88abff1c4e`  
		Last Modified: Mon, 17 Nov 2025 20:00:46 GMT  
		Size: 122.6 MB (122634768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75912c151e3325e3cb408ccc97c2e1dcaa80236a50a2ad093fc4bf0d37db120f`  
		Last Modified: Mon, 17 Nov 2025 23:40:03 GMT  
		Size: 281.7 MB (281666411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f45bec0af0abcd98242d45326c79e1dfe983666e15c9725d5d5da72b727c85`  
		Last Modified: Mon, 17 Nov 2025 23:40:37 GMT  
		Size: 135.5 MB (135521967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82df85eef675ba8493743587d7d1a470465c5c4dfcca8f3637cedcf4a4e9728`  
		Last Modified: Mon, 17 Nov 2025 20:00:30 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:11a35a7340e40fe346720004f368df25b2f2335a9f7d18db6ebbf9e19d105d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9376381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d37cf17af74501f94cca99a92bcfe25f0c78d59f29461d30c150c01a90c25`

```dockerfile
```

-	Layers:
	-	`sha256:e2c6b8651befbaefd60f493d69db426135952401a49d166b1508e4db56ca2b3c`  
		Last Modified: Mon, 17 Nov 2025 21:21:10 GMT  
		Size: 9.3 MB (9346120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233e7f95236641070f918bc39365e4922e41cd04813b1547bcb17a3ce39b811e`  
		Last Modified: Mon, 17 Nov 2025 21:21:11 GMT  
		Size: 30.3 KB (30261 bytes)  
		MIME: application/vnd.in-toto+json
