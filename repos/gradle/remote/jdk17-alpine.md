## `gradle:jdk17-alpine`

```console
$ docker pull gradle@sha256:0de7b876881733c8f48bbdb8bacd3f909c7baf918e52b4503fc9ffbe2d2c6c83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:8b091e6b33a6efb2a0330ba762ea79acbff0641d1d4308495f474b3061f857a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349033196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241b99bddba088ea217a97443defc3bf528533c7ef5c768a6e9f22f8f991d1c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:17 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:58:19 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:19 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:19 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:21 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:21 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:23 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:23 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da2b7fa39d9ca89504884bfa364de57e68f656d1fd46f04941d3d34ffdbca30`  
		Last Modified: Sat, 08 Nov 2025 17:58:43 GMT  
		Size: 21.1 MB (21112255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9308f1b3f4d73b7c1a1aaba0b8eda9e9155caf3619e236d0c1a8b410704ef`  
		Last Modified: Sat, 08 Nov 2025 18:22:13 GMT  
		Size: 144.0 MB (143989616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3851e26ddd2575c157cfd1ad2a673f8e8b4541dd5f6a0b8a2f65d3935e10fe6`  
		Last Modified: Sat, 08 Nov 2025 17:58:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03fcaf37379fff8027b1eaf41f78daa4bf57cd4f423a9e9d7015d3bbcf9bb53`  
		Last Modified: Sat, 08 Nov 2025 17:58:39 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd140e3a584fd1bbe5d9395ae0ebe8e22adabdd7a976dd7e45344a72dac0b023`  
		Last Modified: Mon, 17 Nov 2025 19:58:49 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8ddfd825fd79d70c6c4afc9b386529da0d21566145c17a72291206eda4fe48`  
		Last Modified: Mon, 17 Nov 2025 19:58:55 GMT  
		Size: 44.5 MB (44549039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e33870598c6afa12919b2cb1dd50e83fa334c4a8d85fe74fbe6ddfd3ca3bd47`  
		Last Modified: Mon, 17 Nov 2025 21:32:30 GMT  
		Size: 135.5 MB (135521483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150645aa145a1d7f18a4ebf70ca7b6181a66a7a40495d7b647344f57464e4885`  
		Last Modified: Mon, 17 Nov 2025 19:58:50 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:0265464fa8c2f4bf483d5fa921a41093a8300ae416a9a4c2bf81cbfbd3efe021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dd0774b9cb3a6ffe0671b4b2c83916f136c134ff721b08e041cce8c1ef5099`

```dockerfile
```

-	Layers:
	-	`sha256:a6a89fe1166651ec153f6f26c6c98010701f9745c64cc2cd48c01023411f71e4`  
		Last Modified: Mon, 17 Nov 2025 21:23:10 GMT  
		Size: 4.7 MB (4702978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2584c468867583fe10d4d7f6aa21abbaadb656d4a78b8f5e69e03b0a039fa5f`  
		Last Modified: Mon, 17 Nov 2025 21:23:11 GMT  
		Size: 22.6 KB (22638 bytes)  
		MIME: application/vnd.in-toto+json
