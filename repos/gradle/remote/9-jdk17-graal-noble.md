## `gradle:9-jdk17-graal-noble`

```console
$ docker pull gradle@sha256:40f0cb01f7de6f45d2bc1429a572bc0d6a4517b67f2848d8321c5c359a91e639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:ed835fbe9921dac592fd2379dd2ece3d80a3d2e58b76262454164c9dc1cc0ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.9 MB (608878005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd672cdb43909a2e6ab7d6eeac60a59d0725ec275075200a3c109c216584362b`
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
# Fri, 30 Jan 2026 17:45:02 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:45:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:45:02 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:45:02 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:45:02 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:45:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:45:41 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 30 Jan 2026 17:45:41 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 30 Jan 2026 17:45:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 30 Jan 2026 17:45:50 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:45:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:45:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:45:52 GMT
USER gradle
# Fri, 30 Jan 2026 17:45:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:45:52 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87187573ebd7c1099503249a2fc3a4c6552c22f8b55f8fec4aa6ed359c8b5047`  
		Last Modified: Fri, 30 Jan 2026 17:46:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6a7be14cce7566ae545a02ed1e3685ebdc6c75cefe8515faafaf8b7e8f8c9e`  
		Last Modified: Fri, 30 Jan 2026 17:46:30 GMT  
		Size: 151.0 MB (151041312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce75182ee51de54744dbdd014d8fd0aab21d7dd71f9351a6aa7cf5cc1f2d611`  
		Last Modified: Fri, 30 Jan 2026 17:46:33 GMT  
		Size: 291.1 MB (291064067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1522386ccfed95f35317bcb3cd59efb7991b5568b4885de4acac5eff07434e5e`  
		Last Modified: Fri, 30 Jan 2026 17:46:31 GMT  
		Size: 137.0 MB (137019691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43adc7f0550f28b9d650d3ac5c40a734dad9c8d5996db2359fb45c4b4b373faf`  
		Last Modified: Fri, 30 Jan 2026 17:46:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:8eaff4144c41f1f832f852a59f51270e0d5c6ea1c2f632f6d5581036b7521035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae2920165081321a748a6114e175a3efcba6b95b4fd03a10ed23fb792d08796`

```dockerfile
```

-	Layers:
	-	`sha256:5a101d279bb60b320ab6daab515532fbdec14a30e6325ba3178887a2858ebf35`  
		Last Modified: Fri, 30 Jan 2026 17:46:24 GMT  
		Size: 9.0 MB (8992704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8641c433cb4ab09c32b5d4b2e3b795aa75ec6c3bab904a693309dec940c95c75`  
		Last Modified: Fri, 30 Jan 2026 17:46:23 GMT  
		Size: 29.1 KB (29052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a1e4aa77e82cd0f3d90d211c5cf75d76fad53d286a78c6c64e391edbc12eb942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595378682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b402a7f1b81f4bdda064a7fdb8cce25f4d6ca752a19f9adccc572e4b80a56a8`
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
# Fri, 30 Jan 2026 17:44:39 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:44:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:44:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:44:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:44:39 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:45:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:45:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 30 Jan 2026 17:45:13 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 30 Jan 2026 17:45:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 30 Jan 2026 17:45:24 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:45:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:45:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:45:26 GMT
USER gradle
# Fri, 30 Jan 2026 17:45:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:45:27 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5703ba5eedf156a8bec65cb61ac1ea36fa739190f2ba127ef5893e6063553ec2`  
		Last Modified: Fri, 30 Jan 2026 17:46:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e677cc1bfdf81d2550c10a5df36dfffd8c00499fb80320dc185068e19024e30d`  
		Last Modified: Fri, 30 Jan 2026 17:46:07 GMT  
		Size: 146.0 MB (145962606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe3aa30a74cbe02a4e1b757d05fa59cfc88c6c217a731871d7057ede302d42`  
		Last Modified: Fri, 30 Jan 2026 17:46:15 GMT  
		Size: 283.5 MB (283501910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e7b2bc991ddaa11cc329fe126e2e33a0f9b3cdde7e2ea540f98c7f7c30ee5a`  
		Last Modified: Fri, 30 Jan 2026 17:46:07 GMT  
		Size: 137.0 MB (137019692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed622a4e82ef3a60aef9d392f94c80029ec471f346b52ff9f2ecd5ebead1603`  
		Last Modified: Fri, 30 Jan 2026 17:46:01 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:0a968f2cf2812b69cf701bce7e252f6af98979cbc05d436c24b5fc787650fbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b2088318931b587013451ede6481f792f9af1bb6422555cb1661d07111c25a`

```dockerfile
```

-	Layers:
	-	`sha256:1a3ef4d8238c85c539de3a8d7bc03fc2b1f4cb8ef7cee3ed8cd4fe3e3f895457`  
		Last Modified: Fri, 30 Jan 2026 17:46:00 GMT  
		Size: 9.0 MB (8988285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0168e11fa6d0006c97c53e349e2e42ac98688e7dec0db47081cf6141119b0f8`  
		Last Modified: Fri, 30 Jan 2026 17:45:59 GMT  
		Size: 29.3 KB (29264 bytes)  
		MIME: application/vnd.in-toto+json
