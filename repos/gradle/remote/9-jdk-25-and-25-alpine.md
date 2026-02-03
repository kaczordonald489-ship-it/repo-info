## `gradle:9-jdk-25-and-25-alpine`

```console
$ docker pull gradle@sha256:2cb62a2c2db90f45921db032d85cc545d0caeb2967a9663040a8f0d91f1c0bc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:c9127d67974f5c0951f2b401e28acc209b027fd01119b64b77bdf2dd342f65e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b4dd3b6ee9a41d27e21483a277ac6aec9dfd3f30198a33675dbab74f00c822`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:13:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:13:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:13:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:13:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:13:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:13:56 GMT
CMD ["jshell"]
# Fri, 30 Jan 2026 17:42:52 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 30 Jan 2026 17:42:52 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Fri, 30 Jan 2026 17:42:52 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 30 Jan 2026 17:42:52 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:42:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:42:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 30 Jan 2026 17:42:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:42:52 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:42:55 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:42:55 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:42:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:42:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:42:57 GMT
USER gradle
# Fri, 30 Jan 2026 17:42:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:42:58 GMT
USER root
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c82c37cc1e371eead2dc58300215ff956e7c66f7a9be860363938c03e5c76da`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 14.2 MB (14246382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31aa63af3fdb098e136e53cb2a136db5e58d0d583a45a29aa0f688e2b0c3b3`  
		Last Modified: Wed, 28 Jan 2026 03:14:13 GMT  
		Size: 91.3 MB (91279981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e456b61d1dd1581cd1136ee74763eedb7bf7af1158ecad882564104548359d1`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331024c35ae2ab78ba266cd395ff3155e7a3135687cde5017449ef802da8d926`  
		Last Modified: Wed, 28 Jan 2026 03:14:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc30a066aab261b3f0b4a560aecd2e80d9c7791c7a9944eb3bdd44a5c510ff5`  
		Last Modified: Fri, 30 Jan 2026 17:43:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a378cb7cd0e056a7d9589d5f10235199ffe6c1c0efeeb34416e7325f8d6113`  
		Last Modified: Fri, 30 Jan 2026 17:43:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8962b4aa06d22ae5dfe92dc132eea721cce74e43066670f8be435b8338862b9`  
		Last Modified: Fri, 30 Jan 2026 17:43:14 GMT  
		Size: 46.5 MB (46549363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2612c414e1915323902dcea87000220575ce0112179fba2543701e2388aaaad6`  
		Last Modified: Fri, 30 Jan 2026 17:43:17 GMT  
		Size: 137.0 MB (137019937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d700bae2a1947ac5b99e18a29d166fd1a48da1e040719b5b0b136ea4d9dde67`  
		Last Modified: Fri, 30 Jan 2026 17:43:14 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:5d63c792ada04747e9d314558ba70525b4898fefd5782dc488294b1ca3562fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4615674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835c7daa15ee9514ffb1adf4ac15ca39199151ab1bd3f7504c2fc4207c0e7c9f`

```dockerfile
```

-	Layers:
	-	`sha256:9cfd6aa579ed992b5b5cd82a873b084be3b05e660a2fb02603d450d813d9f3c2`  
		Last Modified: Fri, 30 Jan 2026 17:43:13 GMT  
		Size: 4.6 MB (4587365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33bd3f7ce656f26e5396573c2a568beb5f97f99d20203a9321dc9aaca100893`  
		Last Modified: Fri, 30 Jan 2026 17:43:12 GMT  
		Size: 28.3 KB (28309 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0bac1a6fe86748af86118f79600fcd2e1adb99b7b6aa5548943044df12681dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291812117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625cffed7af570a598ff6c09932c8c8c70ec9290e5a02cbcc53f53415e38a76b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:00:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:00:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:00:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 03:00:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:00:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:00:54 GMT
CMD ["jshell"]
# Fri, 30 Jan 2026 17:45:02 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 30 Jan 2026 17:45:02 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Fri, 30 Jan 2026 17:45:02 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 30 Jan 2026 17:45:02 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:45:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:45:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 30 Jan 2026 17:45:02 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:45:02 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:45:05 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:45:05 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:45:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:45:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:45:08 GMT
USER gradle
# Fri, 30 Jan 2026 17:45:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:45:09 GMT
USER root
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5288573acdcd1544c20a13292ab18c2f63bfc25bd67e4ff7fda45bcd6ff95602`  
		Last Modified: Wed, 28 Jan 2026 03:01:09 GMT  
		Size: 14.4 MB (14352508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59a6d58393b4efd9f9346f830fb5d4b12d5abe806a5efe2b15f408c79a26081`  
		Last Modified: Wed, 28 Jan 2026 03:01:11 GMT  
		Size: 90.2 MB (90190699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452efb31da7be8de7a686fffee1b06489e32b6b26a07b4b1108bee8041a3e12`  
		Last Modified: Wed, 28 Jan 2026 03:01:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a8435556e3b5786f56d544bb393ce6a392d6617de1793d08481767d196bd9d`  
		Last Modified: Wed, 28 Jan 2026 03:01:12 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df858e0cc1201c06c9dad7bec49599ae9fe886b8b9fb98c89bae69530c16df`  
		Last Modified: Fri, 30 Jan 2026 17:45:24 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec52b6c05b824b48472a5d6a74695712920ab93cbbc63093b9eb38fbfbc0ef8`  
		Last Modified: Fri, 30 Jan 2026 17:45:24 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d22fadde74d865d01b714397a4bc70595fe07e2b3653d2ff6417307c8602ac8`  
		Last Modified: Fri, 30 Jan 2026 17:45:26 GMT  
		Size: 46.1 MB (46076441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25960b5640c67978b10dc5448725134035995e20c1f9d7877e10db6fa4c4cbe1`  
		Last Modified: Fri, 30 Jan 2026 17:45:29 GMT  
		Size: 137.0 MB (137019871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cc2cd4a179fd0c77e528409b0b3eda920df311c452333b9e428c148631f8a5`  
		Last Modified: Fri, 30 Jan 2026 17:45:26 GMT  
		Size: 29.3 KB (29348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:6a64eaf9c9d4709a5606af8c8e14050106352d094a04346040e452c8a2424a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90b54e4f14ec1f371243aea84906ed373c182673498add5986598c28eb5f963`

```dockerfile
```

-	Layers:
	-	`sha256:ba89d2d0ca0bb5aec41f9811455864c989a94d544ff68c569d52990295af5bd6`  
		Last Modified: Fri, 30 Jan 2026 17:45:25 GMT  
		Size: 4.7 MB (4737538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75967f821bf24edeba371b778bd4fdb17283cf871d0cdacb33cd08db13e4a10b`  
		Last Modified: Fri, 30 Jan 2026 17:45:24 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json
