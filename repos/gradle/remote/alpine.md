## `gradle:alpine`

```console
$ docker pull gradle@sha256:945b2683d52c62c6d5eb8b01efb59a3653a374a7a50c7c4030b6c7d9f173d90e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:alpine` - linux; amd64

```console
$ docker pull gradle@sha256:96b1e5703b6cdfe9ac800560513c32841bc75cf973dfd5916f1754979ca72b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292930051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba202e061b8f6da3a27788997f509fcf71dfd1810fcf1575d205d87a18d6572`
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
# Fri, 30 Jan 2026 17:43:38 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:43:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:43:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:43:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:43:38 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:43:40 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:43:40 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:43:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:43:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:43:42 GMT
USER gradle
# Fri, 30 Jan 2026 17:43:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:43:43 GMT
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
	-	`sha256:87a8066eae95545d103c390d8b81e6f05f597528b75391bd16912a0dced77b4a`  
		Last Modified: Fri, 30 Jan 2026 17:43:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63ebbb8466d1414f2bd96b65d741080ecfe93c66a6ed45e41b5f2ff4a4f93d4`  
		Last Modified: Fri, 30 Jan 2026 17:43:59 GMT  
		Size: 46.5 MB (46549915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0622561953f51b71fb2cca9a7271db097d255e270e583b1d232609e0f01197`  
		Last Modified: Fri, 30 Jan 2026 17:44:01 GMT  
		Size: 137.0 MB (137019828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9903f4a9e348cb5bd9841afb9ef7205adcd75347beb65f58d7a37ca36766d2`  
		Last Modified: Fri, 30 Jan 2026 17:43:57 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:973b1a37ee821c844614ea8099a22295d5d7d367707a2992433adae4241fd0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4613476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3929c1809cdbb9ff9051813c27cac036b6257ad527c4dcc3ccec23b71a39327b`

```dockerfile
```

-	Layers:
	-	`sha256:e8e02e8d6a087945c53eadc8a5ad26501647bb67591ef08b35a211adcb883904`  
		Last Modified: Fri, 30 Jan 2026 17:43:57 GMT  
		Size: 4.6 MB (4588389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7a3509325b382ba10f3b10b345c1d8be57d53cb549b48da7cd91d3261254ad`  
		Last Modified: Fri, 30 Jan 2026 17:43:57 GMT  
		Size: 25.1 KB (25087 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bf0dca012285b64d29633a789a7566a60ab1e358a6103dd487721a0b23e637cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291811574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079db66bc33b1dffd61213d55645743db9152fcd3b6613ccc7cade28de64f981`
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
# Fri, 30 Jan 2026 17:44:04 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:44:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:44:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:44:04 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:44:04 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:44:08 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:44:08 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:44:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:44:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:44:11 GMT
USER gradle
# Fri, 30 Jan 2026 17:44:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:44:11 GMT
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
	-	`sha256:2d27e2163624f0ac59cf0de19044c1baadc4701585847c3bcde819ed55b2036d`  
		Last Modified: Fri, 30 Jan 2026 17:44:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0897227c92bab9b1ff59f84f9d7d93bb454c6dc1e13e624743a612e1a6afb65`  
		Last Modified: Fri, 30 Jan 2026 17:44:29 GMT  
		Size: 46.1 MB (46076180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb073cd6037a78120112ffe6a9e4db82a59ef86b1e294d30481a40daf4b5e2b`  
		Last Modified: Fri, 30 Jan 2026 17:44:31 GMT  
		Size: 137.0 MB (137019871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35037923a6b06097e9f748ab4036c46e6ab38db0746868f026460622912e173`  
		Last Modified: Fri, 30 Jan 2026 17:44:27 GMT  
		Size: 29.3 KB (29345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:7215df3823b89957bad32a4f0fdda4725049e558f525f762229a0ca820a849f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4763943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78debec8b7d7b6fd0b69cf2a931e1d151de69066720b6c127f06b8cbdac76a35`

```dockerfile
```

-	Layers:
	-	`sha256:5b2d8920880b7dfb6678334f064b790d070185b47f5e17ba3894cae660e34c39`  
		Last Modified: Fri, 30 Jan 2026 17:44:27 GMT  
		Size: 4.7 MB (4738610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ba9cdc2b2c644f64f938f87ba3d0750ed7cab659c7fe772a26473fbb62a30a`  
		Last Modified: Fri, 30 Jan 2026 17:44:27 GMT  
		Size: 25.3 KB (25333 bytes)  
		MIME: application/vnd.in-toto+json
