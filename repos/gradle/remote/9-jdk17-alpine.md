## `gradle:9-jdk17-alpine`

```console
$ docker pull gradle@sha256:94dcf26f3999e0786e308c099e3da27b0a5cbe50dd60813291f32bf2619a9a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:9-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:62841b7db00e7f95b6f07903f935cb0afa4e26ff793f6f61f06675ed3a551320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350528676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c8e8362c399723317ea0bde5f9b4b5f8495aa488b484364442f25f006ff674`
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
# Fri, 30 Jan 2026 17:43:33 GMT
CMD ["gradle"]
# Fri, 30 Jan 2026 17:43:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 30 Jan 2026 17:43:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 30 Jan 2026 17:43:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 30 Jan 2026 17:43:33 GMT
WORKDIR /home/gradle
# Fri, 30 Jan 2026 17:43:35 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 30 Jan 2026 17:43:35 GMT
ENV GRADLE_VERSION=9.3.1
# Fri, 30 Jan 2026 17:43:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Fri, 30 Jan 2026 17:43:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 30 Jan 2026 17:43:37 GMT
USER gradle
# Fri, 30 Jan 2026 17:43:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 30 Jan 2026 17:43:38 GMT
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
	-	`sha256:4ed8caa7aa37a7fbd9ff548286e0e09e4c81f14b65b8d986306aeb8287fb07ca`  
		Last Modified: Fri, 30 Jan 2026 17:43:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28897fbfc5dc52c3abdd44f9ea8f37ab554b5adbfe9aa853fcc8b8704eb3deb0`  
		Last Modified: Fri, 30 Jan 2026 17:43:56 GMT  
		Size: 44.6 MB (44569897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab294777d89952c2c24709e9978d47ab1b20cbba965f35ed6c7cbbcff2196e`  
		Last Modified: Fri, 30 Jan 2026 17:43:58 GMT  
		Size: 137.0 MB (137019854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d245c8e249b01ba3fb102ce17c7c09de88ebca60048504650c23135ef18872`  
		Last Modified: Fri, 30 Jan 2026 17:43:54 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:4b9c6c93c768013b9fc7e610af966873aefb9cd206472e300d047a6a35919065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4714579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816aa66245f5ac4ceddbce2f41d18ab0c2d5835c3e54ac200d0158bd29aee3d0`

```dockerfile
```

-	Layers:
	-	`sha256:f886d472036356f7fa576b5955d8e8c563483c3e4c58a4418743e86ea2467ab8`  
		Last Modified: Fri, 30 Jan 2026 17:43:54 GMT  
		Size: 4.7 MB (4691942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c7fbe6d004fe0ff943d0ce5819f35f6d3039c8755ee8e4b828c398a260085f`  
		Last Modified: Fri, 30 Jan 2026 17:43:54 GMT  
		Size: 22.6 KB (22637 bytes)  
		MIME: application/vnd.in-toto+json
