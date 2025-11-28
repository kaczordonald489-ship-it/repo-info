## `gradle:jdk-lts-and-current-graal-noble`

```console
$ docker pull gradle@sha256:c1c5974f0d44c03de83491cbe9dfb9e229c0bd335a250686c68c788cc086bc26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:8f930b61c23a92cd7027c4e6bb01a4e5041e8bed3571f117be5e26f25fb0f997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 MB (654790386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d5ce59cd7e63769541715f9e53f386b0704c063866a224206912c0a9c2fda8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:59:39 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 17 Nov 2025 19:59:39 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:39 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 20:00:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 20:00:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 20:00:13 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Mon, 17 Nov 2025 20:00:13 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Mon, 17 Nov 2025 20:00:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.1     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.1     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 20:00:24 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 20:00:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 20:00:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 20:00:25 GMT
USER gradle
# Mon, 17 Nov 2025 20:00:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 20:00:26 GMT
USER root
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead290268e33ed6c762a19c60daaa7725a7e651a1f99f556615b3f80653b9977`  
		Last Modified: Mon, 17 Nov 2025 20:01:22 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0dfd58e4d4cfb435b44b82ca46a141c51fa90fdf2fde25c2c1db60b56905c`  
		Last Modified: Mon, 17 Nov 2025 21:13:18 GMT  
		Size: 148.6 MB (148638115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013e68a9504cc71c7a680eb0183d86fa1a089dbc51b96ef763bbceb5e7618b23`  
		Last Modified: Mon, 17 Nov 2025 21:13:19 GMT  
		Size: 340.8 MB (340849262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d2f6cce48ee7acfddc2c10712ce191cfee38422c5110031e90dd1781bb2eb`  
		Last Modified: Mon, 17 Nov 2025 21:13:36 GMT  
		Size: 135.5 MB (135521968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a1db0205ef4bd3513167719813e0092daa1af2e9ba99c597af35b8edd4d8c3`  
		Last Modified: Mon, 17 Nov 2025 20:01:22 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:da392ae30215ad3c6fcf1d9e0dfb45b136a377bcfe2fe783f01d8867c5be06c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9067237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585240c7522abcf11cd6d9a7b9584b64f659be613b8d40a2207755ef205aefc`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf7834da81cdd959df4d8c636619a9c007cce68048ddabc2f00e937f1b703e`  
		Last Modified: Mon, 17 Nov 2025 21:22:08 GMT  
		Size: 9.0 MB (9028753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be641c22c693950a66fb0d52ca120b85e8b3e3823460a1805fc164b335355056`  
		Last Modified: Mon, 17 Nov 2025 21:22:09 GMT  
		Size: 38.5 KB (38484 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f68c389693d8c97c7250faaeb6595524da03d9914f3a9971c2774fe87b6cec4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624079697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d068ab27650e33b86c1955874e9806f4d48555d2ddea4f8e9ec9125c0230b53a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 19:59:25 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 17 Nov 2025 19:59:25 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:25 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 20:00:01 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 20:00:01 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 20:00:01 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Mon, 17 Nov 2025 20:00:01 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Mon, 17 Nov 2025 20:00:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.1     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.1     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 20:00:11 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 20:00:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 20:00:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 20:00:13 GMT
USER gradle
# Mon, 17 Nov 2025 20:00:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 20:00:14 GMT
USER root
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e880a89ce3e78507faac8bded21534e5ea6915534a468ec6d25ae555ebed5e`  
		Last Modified: Mon, 17 Nov 2025 20:01:13 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dad94eadcfe761bc5dfe73208497d348068c5dd2ffc3f411d6455f6608f6f65`  
		Last Modified: Tue, 18 Nov 2025 12:36:40 GMT  
		Size: 143.7 MB (143743204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4dbae20ea83b076c32166941416a6c03305749d7b163593034947f89d4afdf`  
		Last Modified: Tue, 18 Nov 2025 12:36:49 GMT  
		Size: 315.9 MB (315891595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0163764956e25649f0e6b779d4300ea556f7972cf0c2607f8118095f8cd79039`  
		Last Modified: Tue, 18 Nov 2025 12:37:23 GMT  
		Size: 135.5 MB (135521969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2448078b6b54411cc22f0cfdb42a795f05d9b043d6e9dc9ff26509bcd9dc04`  
		Last Modified: Mon, 17 Nov 2025 20:01:13 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:bcd2603aecff0f6b3324228b40be6c0b9fadc6eb4404f1c6a0934dd1fe51f287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9062505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0e625983004089896826f3aaac2184ed8eb533dcf6839dfae2da380db6b306`

```dockerfile
```

-	Layers:
	-	`sha256:f2143f7df81cdf99e97c1d3180d08e3139d0419a72485f1c3c360b8461bfa711`  
		Last Modified: Mon, 17 Nov 2025 21:22:20 GMT  
		Size: 9.0 MB (9023713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feb2b1a5342bc71ce0b5f2274698a29e209bef5a08d1914224ba61066c5ef10`  
		Last Modified: Mon, 17 Nov 2025 21:22:21 GMT  
		Size: 38.8 KB (38792 bytes)  
		MIME: application/vnd.in-toto+json
