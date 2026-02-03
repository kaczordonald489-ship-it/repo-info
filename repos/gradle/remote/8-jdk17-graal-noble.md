## `gradle:8-jdk17-graal-noble`

```console
$ docker pull gradle@sha256:619dd5b3c1aac51bb44ccf93e9658a3841f66c815c349a2599a2af681a1a7c97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:dc2b4a69e94722835351c1484b4a30586dcd7bb41ee7671aa3eed81928dd69b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.9 MB (606882766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c429a4d230bab8e8139b0420d501dbd3ea27592610f903ffc1299992ce4eb94`
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
# Mon, 26 Jan 2026 19:18:11 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:11 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:18:53 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:18:53 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 26 Jan 2026 19:18:53 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 26 Jan 2026 19:19:04 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 26 Jan 2026 19:19:04 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:06 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:07 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccefd09b81bdc5ab1086f2847d5a401d0563ebaea17b307a9f03cc946f5b9b86`  
		Last Modified: Mon, 26 Jan 2026 19:19:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85f636a7479f740e4c24f46cf0ae2a4f22a4be145430cd79f884847cbdc28f`  
		Last Modified: Mon, 26 Jan 2026 19:19:48 GMT  
		Size: 148.6 MB (148648203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448400648e7395eb6d620fa7c0bf6426d95d1d0855bf1b0bd4692e50dcb5462`  
		Last Modified: Mon, 26 Jan 2026 19:19:51 GMT  
		Size: 291.1 MB (291064062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dca47d8022fe89a0f6c96d36519cbca48840a78258ad4c9bc2cd70fc578d52`  
		Last Modified: Mon, 26 Jan 2026 19:19:47 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd7cd8e1bae12f2b80a73de887270ec9184e9cc755c3744533196dab3141ffb`  
		Last Modified: Mon, 26 Jan 2026 19:19:42 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:411aa28ca89ba1d756640fbce5601ecca030567376e38c3657d18b084e5c537f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9037162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7c4e8ad3ddec6337f259511360592a1f7d4cd94bdf85c0e017fd80be05572`

```dockerfile
```

-	Layers:
	-	`sha256:df4265a2dfbcd021b8441f6a055b9b946aecb432034e3da0597cafac517dcb2c`  
		Last Modified: Mon, 26 Jan 2026 19:19:41 GMT  
		Size: 9.0 MB (9008852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbfb28ed034cc881992af7d0fd5654e8f8d404195bef9f993dc3be37f960b02`  
		Last Modified: Mon, 26 Jan 2026 19:19:40 GMT  
		Size: 28.3 KB (28310 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c82ab1ff4421667212aeec5999110a932c8cd383a3460bb3035570db7db16c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593565928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f383add3402ef287d549f591d5398666cff0a58b242d2349d4a8fefcbc07eb`
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
# Mon, 26 Jan 2026 19:17:08 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:17:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:17:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:17:08 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:17:08 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:17:44 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:17:44 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 26 Jan 2026 19:17:44 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 26 Jan 2026 19:17:55 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 26 Jan 2026 19:17:55 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:17:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:17:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:17:57 GMT
USER gradle
# Mon, 26 Jan 2026 19:17:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:17:58 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7331eaace49723ea696207a33178335b42f7742f06bd37bf9f4190002db29d`  
		Last Modified: Mon, 26 Jan 2026 19:18:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404aba17f7170c1c378e885553a1bc5cb2bcef3af493c30c7dceb62ac831bad`  
		Last Modified: Mon, 26 Jan 2026 19:18:38 GMT  
		Size: 143.8 MB (143750776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244f7a6cd9e5c82c76daef6dbf2b24f5fc81a83b9d74534dd1a5c70c5ae29cb0`  
		Last Modified: Mon, 26 Jan 2026 19:18:40 GMT  
		Size: 283.5 MB (283502217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53cba55bd46125352f9c2555f43c811862fac8cba2fab68db136dc6931de365`  
		Last Modified: Mon, 26 Jan 2026 19:18:37 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148fb567a603a5597bd843f80ed839ec1f68886488b01ce51c2da9a59deff5e`  
		Last Modified: Mon, 26 Jan 2026 19:18:32 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:c615c5d4f5c3386192cd304c8e791676d38c50c827d9bf742d697ccd793b202e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9032908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4083f07807a98b1e070aa630835bef524a0ab105480fa3494506e71da4827cc7`

```dockerfile
```

-	Layers:
	-	`sha256:02b6a5fb7d4d0417f010627d8495bb0348c75aeef42dc2c8b121df30c22a70f8`  
		Last Modified: Mon, 26 Jan 2026 19:18:31 GMT  
		Size: 9.0 MB (9004409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a0573d3c70e9c62f0687f55f794ec8301106136e7b7b04d8f4d49a7e6ca645`  
		Last Modified: Mon, 26 Jan 2026 19:18:31 GMT  
		Size: 28.5 KB (28499 bytes)  
		MIME: application/vnd.in-toto+json
