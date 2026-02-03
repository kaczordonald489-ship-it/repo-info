## `gradle:8-jdk-graal`

```console
$ docker pull gradle@sha256:8950739ddfaf54e07aca0be1e9f0dfb1b8eaea1c8731c27d63d58a281b6079b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:f088c11f5604fa63563d9fb7f3492abdc67b2740b67a3b038aef8dad59ed6f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.8 MB (605804824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76da01a621f2e8e2241e2224799aab53e5274d4807ee007a375095a30ee30992`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 19:18:31 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:31 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:31 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:31 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:07 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:07 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 26 Jan 2026 19:19:07 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 26 Jan 2026 19:19:15 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 26 Jan 2026 19:19:15 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:18 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:18 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526921e066d2a6b0f96ba88487d049334961bd6567c3eb7878c983a2e8c20eaf`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f5d8666e2b32836f2079c9ef39423948e66eb5a15ad33006f2e295fafbda5`  
		Last Modified: Mon, 26 Jan 2026 19:20:05 GMT  
		Size: 148.6 MB (148648434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed8d1d0603f37084ef7c5c0e24889b55449b2d7b42e50ec844b1e3d72429c3`  
		Last Modified: Mon, 26 Jan 2026 19:20:10 GMT  
		Size: 290.0 MB (289985892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87f52ae4e4e5eada0afc11992256525b1f4e860af68091ab54cdcc984241e91`  
		Last Modified: Mon, 26 Jan 2026 19:20:05 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc0eafdbc707f76397ba759b04b9215643cdd3d4b9242f7920dcdb995152fe3`  
		Last Modified: Mon, 26 Jan 2026 19:19:54 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:4ade4e875f8fda6c71af73e80cfe854f8fafe200362f6b7837cc3f85e383b35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71f190fef495fd24d90e3d5cad6a7fe933ef766f5f6204b6037e2721f20c9e`

```dockerfile
```

-	Layers:
	-	`sha256:877152ad5508486ad466d406a596b4d9a69e30d180f2cb7d5a68b2e5b3984374`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 9.0 MB (8989721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c847258e492102ac9f3348aff7bbcb1db83ca8b85b594f5520b40ed33e16aa7`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 32.0 KB (31995 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:21749b72870a9e42a783a3b4a7673bf3d28af403839e8c69f1ea789593f30221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591729703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155980967ec256bc19ea172533a5a95a16cd463b3f90dd48c5c33b4dbea5c5b3`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 19:18:42 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:42 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:42 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:42 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:17 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:17 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 26 Jan 2026 19:19:17 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 26 Jan 2026 19:19:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 26 Jan 2026 19:19:26 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:28 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:28 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c9c1e4ce98dbc44b6bbab58c0c7ac487aba9d274236403096258602be0bb9e`  
		Last Modified: Mon, 26 Jan 2026 19:20:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9059e69f9c2f5c574a2f0101fbf2a2ca4f2041a001ce2a9125f82f2811be46`  
		Last Modified: Mon, 26 Jan 2026 19:20:13 GMT  
		Size: 143.8 MB (143750608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4447d41dcfc1a45b3582fd5a2bba9d6c57e8cc8b6410dab14e87afa54556fb2f`  
		Last Modified: Mon, 26 Jan 2026 19:20:18 GMT  
		Size: 281.7 MB (281666159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ab3bd2fb511369a5ed492ae85c534913f322bd4288d3650de3f587d2fcc59`  
		Last Modified: Mon, 26 Jan 2026 19:20:14 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e067cc3e8c4bf9329d4337cdc24529b577bd1e930996ffd047e93b25e46393`  
		Last Modified: Mon, 26 Jan 2026 19:20:08 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:705ddc8e4d47cb59af9f58dcac00b0fc69202bba8e17304a17b8dfc4fc7be151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743fe21dd728d939ab174c4d59db1cd62ecc4d76710d4dfe749b7058bb50873`

```dockerfile
```

-	Layers:
	-	`sha256:a24cf5e72d35455ee7be5c9f5e09c203a00dbe663326ae69cae2e9a5b22f0cca`  
		Last Modified: Mon, 26 Jan 2026 19:20:07 GMT  
		Size: 9.0 MB (8985426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8b049737d3b7dc554bb3f7c02f7545ddf1a871c2f5bb85f63dbea9dba1a0a2`  
		Last Modified: Mon, 26 Jan 2026 19:20:07 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json
