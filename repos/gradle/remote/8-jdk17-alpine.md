## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:540f01bf952e6d90fd1105c51bdd6dba7bee83958cbec6c17023b29c259b5e1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:27cc256c732cc7843e5f1ea396a9dc61e290d35ed0776cfde2904ff7f06ba61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350479491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c2351cd4ce92b3da1b7621f1593a7b7e557c534b90e43acd77607e7b713f3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:06:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:06:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:06:56 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:07:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:07:04 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:12:16 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:12:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:12:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:12:16 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:12:16 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:12:18 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:12:18 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 28 Jan 2026 04:12:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 28 Jan 2026 04:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:12:21 GMT
USER gradle
# Wed, 28 Jan 2026 04:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:12:21 GMT
USER root
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77cdbd7bc1e2f452d8429402632b993034ee6bfccffc10cc8a951d8f9bf6b4`  
		Last Modified: Wed, 28 Jan 2026 03:07:19 GMT  
		Size: 21.1 MB (21115424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db795874e1acc8dcd7dfaa11e545c47a36bd9db774d51cecf4ab0273da86053a`  
		Last Modified: Wed, 28 Jan 2026 03:07:22 GMT  
		Size: 144.0 MB (143989559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cba3796c63f930fa19b62040f34d6b16b4f7dd6a95896d3e6da8c177eabd7`  
		Last Modified: Wed, 28 Jan 2026 03:07:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357173fc29013c94bdde74c736de14f4dfaf05e42614f5d5346add87083f20f3`  
		Last Modified: Wed, 28 Jan 2026 03:07:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dfc7c9aae9964a66665be139dc98516032df5bad75457855c043f6b681511`  
		Last Modified: Wed, 28 Jan 2026 04:12:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097081a93dd83f7b99e12f1d1df9e877437bbe7d0bfb72828b6d8955fda8b14a`  
		Last Modified: Wed, 28 Jan 2026 04:12:40 GMT  
		Size: 44.1 MB (44123025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9528a7c288b7f3e147f178d044aa9d21f5c1dc433d1f2e04eceef82a716d7a`  
		Last Modified: Wed, 28 Jan 2026 04:12:47 GMT  
		Size: 137.4 MB (137388247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9a6a6853b4f785f90e6db9f8f113d92dafd1a551edaa1515155ebcd04437a2`  
		Last Modified: Wed, 28 Jan 2026 04:12:38 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:56b27dfbef3bff5dad20e4530c90ac46401b6c4adb899bae0ec4f9f5842b433b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4726097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf50c00e63765a7b5479dff8e443a0d4efac09b8a3dde3820cfaace189455cb`

```dockerfile
```

-	Layers:
	-	`sha256:e8c7016007bf4b2e902cd2082b19b4f8d09b9168992346ae75053e0ab32b216b`  
		Last Modified: Wed, 28 Jan 2026 04:12:38 GMT  
		Size: 4.7 MB (4703946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbee3a2f4d08f913c5794ad4ff2be902273a8d8442f719681a8843b8ef629c85`  
		Last Modified: Wed, 28 Jan 2026 04:12:38 GMT  
		Size: 22.2 KB (22151 bytes)  
		MIME: application/vnd.in-toto+json
