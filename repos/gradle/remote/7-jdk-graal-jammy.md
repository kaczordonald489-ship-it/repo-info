## `gradle:7-jdk-graal-jammy`

```console
$ docker pull gradle@sha256:267f373355ca915c99d7286996249873ab1f0481dca0bb4a41c1603587d5a178
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:183be13f905889c7b6c1b1c40c942df5db90d8f17ad27266b92bb4cadb4daa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575682530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3c9e26031cb8de71ec623337c2a5f2b050696ee93f1d9ac65c5c4e039bb51e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:21:32 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:21:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:21:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:21:32 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:21:32 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:24:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:24:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:24:16 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 15 Jan 2026 22:24:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:24:26 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 15 Jan 2026 22:24:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 15 Jan 2026 22:24:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:24:28 GMT
USER gradle
# Thu, 15 Jan 2026 22:24:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 22:24:28 GMT
USER root
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7270d75d9e40bfb5daee9852b7f9bd0f148f1dc0369bcf3ead27f555fb0f0a`  
		Last Modified: Thu, 15 Jan 2026 22:22:45 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9af7d3bedd42ff4d8b3c77fa7b7d5df0aeedc29059d369ad3a2a3816b250bf`  
		Last Modified: Thu, 15 Jan 2026 22:25:05 GMT  
		Size: 126.6 MB (126553146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7005f4f8e0ad8f7a6ee6062208ac4d4b566902311bf995cda3a55598aefb7a27`  
		Last Modified: Thu, 15 Jan 2026 22:25:11 GMT  
		Size: 291.1 MB (291064068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5a89dbaff0067cf22ae3896c35545de3df96d0d70fb66ecfc2eaaa81a04ea3`  
		Last Modified: Thu, 15 Jan 2026 22:25:06 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae0b3b1049365b97bd9deddd92892cf5e316a17360eb8cf2cea0bfa8a8cd68b`  
		Last Modified: Thu, 15 Jan 2026 22:25:01 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e24ef6749b2d079d2b3317201f76f16fefd514162fdb69c65ae985597884bcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82656741c4d78aafb78d59b07ada525c1e8a015fc35d4233a8ff28b6a1921343`

```dockerfile
```

-	Layers:
	-	`sha256:32cc2695bfb601e90beeb45eaf65fbc20d301074131a1f33a38c2451fc246cb8`  
		Last Modified: Thu, 15 Jan 2026 22:25:00 GMT  
		Size: 9.3 MB (9315622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5413c2be6a43a2359614682594c461c7dc265b6d4a0abdbd6fdad0e7c29dbd`  
		Last Modified: Thu, 15 Jan 2026 22:24:59 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0f979a8ea81924f799f2f205dddfeee2e06580cce6d8311d028f0af1cf86a81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562066212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5411d215d82dda16bff99c5607b66fa44cb9625795ddc96a59c12a7605793c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:26:22 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:26:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:26:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:26:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:26:22 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:26:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:26:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:26:54 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 15 Jan 2026 22:27:04 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:27:04 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 15 Jan 2026 22:27:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 15 Jan 2026 22:27:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:27:06 GMT
USER gradle
# Thu, 15 Jan 2026 22:27:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 22:27:06 GMT
USER root
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0079e8a2026f17f21be2ce12d5f954c66b19eb2fe6993d30eefc5e2e5933ac`  
		Last Modified: Thu, 15 Jan 2026 22:27:38 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397d7f6bc436218fb1d10d5611c9848a86298841808cfb175feb1ce693d6d7aa`  
		Last Modified: Thu, 15 Jan 2026 22:27:44 GMT  
		Size: 122.6 MB (122647518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc94a13a65e2267056e794fe0819b8c80e49bb98c272e4aa37da521ff809e5ad`  
		Last Modified: Thu, 15 Jan 2026 22:27:47 GMT  
		Size: 283.5 MB (283501921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12214ce61bfc6a4d21e63a699474323dbc053f42fb4ddf41f0b94c7e91936455`  
		Last Modified: Thu, 15 Jan 2026 22:27:44 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60b0e1e565757a61588504a776a1697f8ea05874dcb46b7f81e8e4709d88bdb`  
		Last Modified: Thu, 15 Jan 2026 22:27:39 GMT  
		Size: 59.5 KB (59516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:3b06e68823bbbd5ffda18046ad97fab2520e4004f91b3e007c5965b0b6173c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9313696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf1863e0cbde7bd9b3888726e650f9d597290ade2f92676ebf7e94c5ceeac90`

```dockerfile
```

-	Layers:
	-	`sha256:b5786703f50d867da7d8e8bd44e923ca5a56ca5cf515349a67a1c90efcc4fabf`  
		Last Modified: Thu, 15 Jan 2026 22:27:39 GMT  
		Size: 9.3 MB (9284438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f784cc0f834f2875c033f4ea34ad5715ffb10cb7333f9d88383c8c4da82880`  
		Last Modified: Thu, 15 Jan 2026 22:27:38 GMT  
		Size: 29.3 KB (29258 bytes)  
		MIME: application/vnd.in-toto+json
