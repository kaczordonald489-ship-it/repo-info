## `gradle:jdk-alpine`

```console
$ docker pull gradle@sha256:f4574d501ead999a718305d165f21099f1e3de08832c33ca5293f816b4ba7794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:d53e456a954e3d5ac9ed6ba9c2a2a772f052f31f8fe37554ade674ca9bd64b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291468338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fedd81ae4e0e5fe9e6bb454e62f9da0d11092c7d40251dc43fda8195540e02`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:11 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:56:10 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:56:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:56:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:56:10 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:56:10 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:56:12 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:56:12 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:56:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:56:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:56:14 GMT
USER gradle
# Mon, 17 Nov 2025 19:56:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:56:15 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ab655b026e5703579820f0d4485d514c6ec9d4b5b462890ac71da2da0ae46`  
		Last Modified: Sat, 08 Nov 2025 18:00:40 GMT  
		Size: 14.2 MB (14245329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f1a65d0fae852f6718306326728109ed1ddecfbfd653037dda93a9669e4a7`  
		Last Modified: Sat, 08 Nov 2025 18:00:50 GMT  
		Size: 91.3 MB (91279717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f288373361582707b01fea1abf34f4ff1053f3baee5acb21cf34af46e4f8c85`  
		Last Modified: Sat, 08 Nov 2025 18:00:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3137254c0a4b1b24ea31eeee2f470985f40fee31365b16a41a6d5745dac38`  
		Last Modified: Sat, 08 Nov 2025 18:00:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556b061502073079b5f58fdb26d05ebc227c0fcd6d7752e50fe338d08f6d2ff4`  
		Last Modified: Mon, 17 Nov 2025 19:56:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9774c76d5b03bddb816401c444ed4b13ba1c0db1d75464620e08cd470fc28d0c`  
		Last Modified: Mon, 17 Nov 2025 19:56:51 GMT  
		Size: 46.6 MB (46560970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025e4969b4dc42ce8bb1b885e3de8099db64d7523143c345bae34f133c01921b`  
		Last Modified: Mon, 17 Nov 2025 21:34:48 GMT  
		Size: 135.5 MB (135521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d3c4fd14fd8d48a0910500a58a3577451d2a24afae2a25fe5baf58830545b7`  
		Last Modified: Mon, 17 Nov 2025 19:56:43 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:3a424a86e5b95bd88dd5f628e88cb2d3eadc4f4da21f1e1feac8a382360897a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4624513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdca1fc94dbfaed9abdec7d384a8ab27d8d0b877829db0c03480a6ce6fa0df4`

```dockerfile
```

-	Layers:
	-	`sha256:dba6be7e11d7785e9548a54526a6e0fc59de46cd4081d7d96e5f835d6a2dba5d`  
		Last Modified: Mon, 17 Nov 2025 21:20:45 GMT  
		Size: 4.6 MB (4599425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fb8f04de51d03b504a14fa7951f03971fbf2c38d685b5385d6d70447052ff8`  
		Last Modified: Mon, 17 Nov 2025 21:20:46 GMT  
		Size: 25.1 KB (25088 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0f17d89c5657e159dccd4a14bebca127e705ab6e504b6e0e4fd8a9a28c166ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290336414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586369ac41878557d85237565a7c641fe36e119f32ce4f52d019ec4b0a1d3692`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:59:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:42 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:54:33 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:54:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:54:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:54:33 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:54:33 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:54:36 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:54:36 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:54:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:54:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:54:39 GMT
USER gradle
# Mon, 17 Nov 2025 19:54:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:54:40 GMT
USER root
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b164f8b4d68be083596089650c1556ab1373815abc8abda59bc45d20ffd1c`  
		Last Modified: Sat, 08 Nov 2025 18:00:15 GMT  
		Size: 14.4 MB (14352513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde8e40d136c44f0d23e0b4d7594cae8888c80bed021fac4cf5ebebb75434c1`  
		Last Modified: Sat, 08 Nov 2025 18:21:45 GMT  
		Size: 90.2 MB (90190637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13765a23e62e85c56a5a54b976e0378167533c0495d297bb429a218799ab164f`  
		Last Modified: Sat, 08 Nov 2025 18:00:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c959ab9ac7fdf8f6393c84753f989ef0811ac7c86a2d184030c23e2d067c93`  
		Last Modified: Sat, 08 Nov 2025 18:00:04 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a039b663806118f95cb0211cdc869963666295edd7a6dbe9e531a447a3cd43`  
		Last Modified: Mon, 17 Nov 2025 19:55:06 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5be776e316699be0bbb26042cba22adfa20bd0aff011b5c3ec881aaeefa0c`  
		Last Modified: Mon, 17 Nov 2025 19:55:10 GMT  
		Size: 46.1 MB (46070674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09a7dcc9dcdfcdacba61ceb9e8fc0ca364b11e887dc8787975d29b7fcf65d4`  
		Last Modified: Mon, 17 Nov 2025 22:01:54 GMT  
		Size: 135.5 MB (135521535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cbaaf153b513449bc9609dbcbca8553facc29cbf9f786c1a17670d1615707e`  
		Last Modified: Mon, 17 Nov 2025 19:55:06 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:3bae9ada5c9e8379bd6dd753ed8943b4591232bb55355889a5bc333b9ea5e5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4774979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816b88540d4be129bc5b7626a16285948dd65d09cffbde528f45ed2f8a53dfe7`

```dockerfile
```

-	Layers:
	-	`sha256:67f41e8cbd1fed8ce1767fc352e13bdca7217692607b5c03c21761ea4364caa6`  
		Last Modified: Mon, 17 Nov 2025 21:20:53 GMT  
		Size: 4.7 MB (4749646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd418185560355d432002db949d7aad6dd56410daf252624cef798d3a297d14`  
		Last Modified: Mon, 17 Nov 2025 21:20:54 GMT  
		Size: 25.3 KB (25333 bytes)  
		MIME: application/vnd.in-toto+json
