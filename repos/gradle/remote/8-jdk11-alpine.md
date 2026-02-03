## `gradle:8-jdk11-alpine`

```console
$ docker pull gradle@sha256:314e8e4f90353821a0498079330a3ed47b6be4c710e1f8d06786df60351332db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:5b09fe33a5223100490f0a7b925fa1df4cb8937a249adf28e249327ae0820f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343216108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3640859cfabf86e3ed7b9745c2b3b46ceff098fd4b2c090f5f4c91a601f83798`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:03:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:03:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:03:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:03:00 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Wed, 28 Jan 2026 03:03:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:03:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:03:08 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:12:31 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:12:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:12:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:12:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:12:31 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:12:34 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:12:34 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 28 Jan 2026 04:12:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 28 Jan 2026 04:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:12:36 GMT
USER gradle
# Wed, 28 Jan 2026 04:12:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:12:37 GMT
USER root
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95a7405177abd55077356ffb7a848c87d9ca9c23db8124d028a03a08abbd43`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 16.3 MB (16294011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6a695983e73627cb4159100da7fbc662b3727706c392e8ffd27d64bf481c2b`  
		Last Modified: Wed, 28 Jan 2026 03:03:26 GMT  
		Size: 140.1 MB (140102382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea14b20ff7de2eebe5038d26444bbb80a02022f13817302f2fe29c8cd0628cda`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7aeb83382b9b7198bf601d2ec81a192e153f4aa03d11277731a45d81e1f902`  
		Last Modified: Wed, 28 Jan 2026 03:03:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528db0d141c47765bb7abdde3c0addaa09ee1973f32313735e4b64b6c360dd9b`  
		Last Modified: Wed, 28 Jan 2026 04:12:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496f99718546fe375c3696ed4f5e11cb1fe2f13c6540df7e682e44bb0e413377`  
		Last Modified: Wed, 28 Jan 2026 04:12:54 GMT  
		Size: 45.6 MB (45568456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c259014f5767432e95cae50eb1780246efb96520a795d89710f2d7ee942c77f7`  
		Last Modified: Wed, 28 Jan 2026 04:12:56 GMT  
		Size: 137.4 MB (137388017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afffae744e195ca13c7e5068ba62a043be820342e128a71759c6d2e199e19bbd`  
		Last Modified: Wed, 28 Jan 2026 04:12:52 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e6cc8dff558be92579038e74e594a1363779c6418f1d29b89b2de7dd5b958d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4633016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce6e400bebcd18a0ad0c5f8626d551ad179bfb0f4602fb147a4d2e4d8f909b8`

```dockerfile
```

-	Layers:
	-	`sha256:706186f4190d4d280d61c2d4addce9403e4eec1f5d422123997070fbe9f05493`  
		Last Modified: Wed, 28 Jan 2026 04:12:52 GMT  
		Size: 4.6 MB (4610558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:544551fd5b2e9657f0ed064af939501584080af4c1acb875fb1b7b3fe34e6165`  
		Last Modified: Wed, 28 Jan 2026 04:12:52 GMT  
		Size: 22.5 KB (22458 bytes)  
		MIME: application/vnd.in-toto+json
