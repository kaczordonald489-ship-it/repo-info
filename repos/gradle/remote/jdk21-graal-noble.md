## `gradle:jdk21-graal-noble`

```console
$ docker pull gradle@sha256:a7f1c37ebfe173bb1fe881db33eca455f86a79bf54e8e173d2a43c64333b4296
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:233ff003467895dff10c552aa3f5e80a98b45693e6b0a501ddd23384a5e7e82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.8 MB (607799309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5aff6b7b9232d6d6aa43551ace8b8a04bf61cbe55c67e5a01fdf8c009fd5e`
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
# Fri, 30 Jan 2026 17:44:29 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:44:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:44:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:44:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:44:29 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:45:01 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:45:01 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 30 Jan 2026 17:45:01 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 30 Jan 2026 17:45:09 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 30 Jan 2026 17:45:09 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:45:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:45:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:45:11 GMT
USER gradle
# Fri, 30 Jan 2026 17:45:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:45:12 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a66f507741118f597dba36b2148a44761e831b4ba844af913382741e116b18b`  
		Last Modified: Fri, 30 Jan 2026 17:45:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdfc667d6a39ae69709e32e2d27f21559daadb79b491efa8c5b9cd893ed1075`  
		Last Modified: Fri, 30 Jan 2026 17:45:52 GMT  
		Size: 151.0 MB (151040686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4603d98b8dddd5f7e23d2c39c6f94da22d870529f212dfb70b62c9d3b3fdaadf`  
		Last Modified: Fri, 30 Jan 2026 17:45:56 GMT  
		Size: 290.0 MB (289985987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6783de32407571c191fbda2214ca398f39d5f5f3f11ee15e6df83aac6d24e836`  
		Last Modified: Fri, 30 Jan 2026 17:45:53 GMT  
		Size: 137.0 MB (137019689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc78d7ae4867acf9984ac5730d0ef26be6de75631b62d624b04b5e69c117e81`  
		Last Modified: Fri, 30 Jan 2026 17:45:45 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:1b3157c0def390b60b0250f727f382b08ff25108b53c9fae37be6f570149cc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8998737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb458f1dd98073f4fb7f912ea017f4cb8ca9a78bd1b880ed94dd2842def003aa`

```dockerfile
```

-	Layers:
	-	`sha256:b7c44edbbb0e8dd0e485da1a29ecd938ed9e8c51814c536f478ffbdec20b93b8`  
		Last Modified: Fri, 30 Jan 2026 17:45:45 GMT  
		Size: 9.0 MB (8969789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3587d7f4af6d45a1147f9247c1b74a64116d0eebcd5a3f44075296e90a985f1e`  
		Last Modified: Fri, 30 Jan 2026 17:45:44 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:68d344e6944c87dcef06ba8b99d724f2345a6fc5b5f7c036130c13c24a53fbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.5 MB (593542058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d513fe6a634cc591afb9bfc13beea54f29472ae00a6f3d4a6792fd3569dd35`
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
# Fri, 30 Jan 2026 17:43:03 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:43:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:43:03 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:43:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:43:03 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:43:38 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:43:38 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 30 Jan 2026 17:43:38 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 30 Jan 2026 17:43:47 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 30 Jan 2026 17:43:47 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:43:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:43:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:43:49 GMT
USER gradle
# Fri, 30 Jan 2026 17:43:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:43:50 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1afb4b8dd7490d4a6126c7bbd4a14ad11e82785e08b601d3922c2a569389145`  
		Last Modified: Fri, 30 Jan 2026 17:43:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729295a1ddf7a35480ecd9a0d6fa3022aa555685dda4c1aa390e62009486e9f`  
		Last Modified: Fri, 30 Jan 2026 17:44:29 GMT  
		Size: 146.0 MB (145961699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a8f45b7fd2c967d33029a3817816e9bf68a18863fea233a8dd697a5e04f541`  
		Last Modified: Fri, 30 Jan 2026 17:44:31 GMT  
		Size: 281.7 MB (281666189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ac7cc9d1e322db0cda0863f1256aa99793cecc296c3e5ae1651c1a8a3af82`  
		Last Modified: Fri, 30 Jan 2026 17:44:28 GMT  
		Size: 137.0 MB (137019691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7aef7b234197aff4ccc4ba649ef49d14effe03f9447bf025a027d2cdb5546`  
		Last Modified: Fri, 30 Jan 2026 17:44:22 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:2de85f53f5950f06c4589483c8b7551b83269324f5c57f337fc696b63d080816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8994534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0727d66ea3e98462cf76470dd8ecb33eb3b28d5dc869e636667a2d1b31b6c618`

```dockerfile
```

-	Layers:
	-	`sha256:9ec7bc70468743f264eb446b94083c35aa771d73a49495795370d05f2702025b`  
		Last Modified: Fri, 30 Jan 2026 17:44:22 GMT  
		Size: 9.0 MB (8965374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79d2743e3a8cb36e70b675072ee55f9ceb731d2cc1446614d849d78899477d3`  
		Last Modified: Fri, 30 Jan 2026 17:44:21 GMT  
		Size: 29.2 KB (29160 bytes)  
		MIME: application/vnd.in-toto+json
