## `gradle:jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:60745457b5d2fc50575169cf19f85f2f72c4c809813b61b4e8cc6d2901303a19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:99fbaf4a9313c88350a0c3c827b1c49a16a80747bc779c4b6efbe0eaa1ae94d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.7 MB (582721554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77695a8fd2ddf547c2639b91327f1624d6ec48d073268e2d8b9619fc536bc210`
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
# Mon, 17 Nov 2025 19:58:07 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:07 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:07 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:35 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:35 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 19:58:35 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 17 Nov 2025 19:58:47 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 19:58:47 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:49 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:49 GMT
USER root
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd9c16be417bc765e592e234d17f33f106bde552cd40dfb1f718f458b5e4bf3`  
		Last Modified: Mon, 17 Nov 2025 19:59:38 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0816f8f7c1fc5a4da896e2600d78c3011c06e0bd12a91144068985cc37cef3c`  
		Last Modified: Tue, 18 Nov 2025 09:28:48 GMT  
		Size: 126.5 MB (126539235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbbe230c740a00929940ad125aef525ff46d432eefec5ca2658457011cf75f`  
		Last Modified: Tue, 18 Nov 2025 09:28:39 GMT  
		Size: 291.1 MB (291064316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a69d4bb7526c19dc25681aa673cd57a1ba84c7cfadad8a7c787b6a70d15f77d`  
		Last Modified: Tue, 18 Nov 2025 09:28:45 GMT  
		Size: 135.5 MB (135521968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2ae9dc5e4fb50ea6ae30675c9a68e60fa489b069fb6655e6d292bf2b3c6707`  
		Last Modified: Mon, 17 Nov 2025 19:59:38 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:a16a623f0629402f917463aefcfcd784b3117584ff94a2006c74982cc38d7084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee72e707b8e276cac54e4c460de6966e5e918bdd1eb5dc0039d840a1d7f43a1`

```dockerfile
```

-	Layers:
	-	`sha256:2c2d2ebfc30247e38499397256e2097144d79daa9488513904d427190922e427`  
		Last Modified: Mon, 17 Nov 2025 21:23:36 GMT  
		Size: 9.4 MB (9397635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c839d6652d76ed880ef7b1b507550c350890c47f12794a055f9d70e1f1bdb1`  
		Last Modified: Mon, 17 Nov 2025 21:23:37 GMT  
		Size: 27.6 KB (27557 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ed372a2ff6ef766abbb00b85cfeafb3eaae6323ad7fe5e0f0ca0684ead2e8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569107344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca930b83679148838b2cfcdeb3e2244d233c3933581cbe3f4f92ea72baa96c`
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
# Mon, 17 Nov 2025 19:58:01 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:01 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:01 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 17 Nov 2025 19:58:29 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 17 Nov 2025 19:58:40 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 17 Nov 2025 19:58:40 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:43 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c9954050e5dd57ae487c7fe9f992ba613373d300902ecd32ed33fb02776df`  
		Last Modified: Mon, 17 Nov 2025 19:59:31 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24566ef24c26cebb4d52f1183e997e98cb07022fc08fb58ea693dd4ce97335b`  
		Last Modified: Mon, 17 Nov 2025 19:59:42 GMT  
		Size: 122.6 MB (122635691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4b19b6e24ae174643edd9c6e78b1eefc2849a9916f4de15e26b6bd9818ace5`  
		Last Modified: Mon, 17 Nov 2025 23:38:29 GMT  
		Size: 283.5 MB (283501932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fbcb6d1d272f89e5338b1e6f99ede6fbd4d67d675fd9a60dcd7b875d4fd89`  
		Last Modified: Tue, 18 Nov 2025 12:37:01 GMT  
		Size: 135.5 MB (135521967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606ccac41e908f60070e16dfd71e64d8a0cce055a981a9af525faf639b3d9ec9`  
		Last Modified: Mon, 17 Nov 2025 19:59:31 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:f0a7d3ced8169a3ec3c9fca26795776e5a9ae9311f4986b1280371d0d27686cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234615a356bcc4d151c8159a6863a3b924c20eb9f5bfc6b6448fc625913c327b`

```dockerfile
```

-	Layers:
	-	`sha256:3e5fd80a3c7edd5bd73ec073fb58d65778c8a298bb9ba7a00e690583dfaa0a51`  
		Last Modified: Mon, 17 Nov 2025 21:23:46 GMT  
		Size: 9.4 MB (9366391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3bff3cd93256cac5f367e51305019fad591b0b8a561c47c6658c7b9459efe7`  
		Last Modified: Mon, 17 Nov 2025 21:23:47 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json
