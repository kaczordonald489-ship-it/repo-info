## `groovy:jdk21-alpine`

```console
$ docker pull groovy@sha256:7ddc7b1a455ec071cb63be668ea3c1ad36da5b96131a4cd25fc1f1bcdbd6989c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:fed035aefe8f1cdbe00e2c82bb5a584bd747bec113bdc1bf3e5360ed73046d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217585946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee142ec64934eba131b41c0296c00602b5949949e74f146e8003e137f936561`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 03:11:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:11:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 03:11:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 03:11:08 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 03:11:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:11:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 03:11:16 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:13:20 GMT
CMD ["groovysh"]
# Wed, 28 Jan 2026 04:13:20 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 28 Jan 2026 04:13:20 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 28 Jan 2026 04:13:20 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 28 Jan 2026 04:13:20 GMT
WORKDIR /home/groovy
# Wed, 28 Jan 2026 04:13:20 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 28 Jan 2026 04:13:28 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 28 Jan 2026 04:13:28 GMT
USER 1000:1000
# Wed, 28 Jan 2026 04:13:29 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec9d6adc0e2666316744526b3e6b46024e14d211d934176cc82f480f88468a4`  
		Last Modified: Wed, 28 Jan 2026 03:11:33 GMT  
		Size: 21.1 MB (21115198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c077e7f5dd48795d611a90c0aeeabe7b837252b56c8406aac46577cdbcd6bd93`  
		Last Modified: Wed, 28 Jan 2026 03:11:36 GMT  
		Size: 158.1 MB (158102925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654728b92e1362ff81920038e72b4daebd48183a298e8e2a566bc42aad73110c`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be48a2be2658e4295069ddce05198f142098bc57a82f27d2da35698afdc81`  
		Last Modified: Wed, 28 Jan 2026 03:11:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9916a07b9875d7e0e1bcba1a25d46fec16f552193b56b4e36b70d37b0ef56005`  
		Last Modified: Wed, 28 Jan 2026 04:13:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b70a48e7f9d46fe90d6ce058ebd3a3e86a7b7a8fefdeb2405fba528cae974`  
		Last Modified: Wed, 28 Jan 2026 04:13:40 GMT  
		Size: 34.6 MB (34559336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deda30590faabe06b04c9cb62519c40fddc936b7239ff718bd84b4e938fee2c`  
		Last Modified: Wed, 28 Jan 2026 04:13:39 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:14154f9068fc5b62372e7057dc1144511256a2a8aa12d2123952e0da621cae39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1233883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f71ca6d9b6d414fa175a66940f6de8d087500d1d514a23624ea613d6e731b`

```dockerfile
```

-	Layers:
	-	`sha256:6139a6fd4ba6d342278545c8e447a4ed311b36ad9a99d2c21c22205d8c0c09ee`  
		Last Modified: Wed, 28 Jan 2026 04:13:39 GMT  
		Size: 1.2 MB (1209123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5668956083eb5c6f176045acf75fe1944975ac0458f92419c633bc877da36113`  
		Last Modified: Wed, 28 Jan 2026 04:13:38 GMT  
		Size: 24.8 KB (24760 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:9aea2a8e5ebd3c5c9a84049a87c454329a94fc91976de4b42ae0f0d3a02bc402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215976882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910eb0abfe1266f4ef2bcf80a9cddc66009280e21a2166d7c68b7ea765bb065`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:56:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:56:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:56:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Wed, 28 Jan 2026 02:56:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:56:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 02:56:47 GMT
CMD ["jshell"]
# Wed, 28 Jan 2026 04:35:01 GMT
CMD ["groovysh"]
# Wed, 28 Jan 2026 04:35:01 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 28 Jan 2026 04:35:01 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 28 Jan 2026 04:35:01 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 28 Jan 2026 04:35:01 GMT
WORKDIR /home/groovy
# Wed, 28 Jan 2026 04:35:01 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 28 Jan 2026 04:35:09 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 28 Jan 2026 04:35:09 GMT
USER 1000:1000
# Wed, 28 Jan 2026 04:35:10 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237401997b4e6d77e1a6cbf3006b196170369b2872d0a2fba9f845ce7cfeeb5`  
		Last Modified: Wed, 28 Jan 2026 02:57:03 GMT  
		Size: 21.2 MB (21166024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf8a9ded26681fc49549c27c20edd4b88472a3ca476e9a7c4ebf9d58174315`  
		Last Modified: Wed, 28 Jan 2026 02:57:06 GMT  
		Size: 156.1 MB (156097479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c000864d8ab5dc2884668139fc08c3b2e6cc3aaa69eacd03144943b90354f`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e39acec808282ee08cd7b6292bf85d7b6775f69ca5e3bb0eb617e09e97bb94d`  
		Last Modified: Wed, 28 Jan 2026 02:57:02 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5e6e555113955a019531f32bba01df17e0160b53f34411d0c58f084afffcbf`  
		Last Modified: Wed, 28 Jan 2026 04:35:19 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b191d4978fc1c3106539599db18884d7bd0c859926d3a2406d7bc2f271884`  
		Last Modified: Wed, 28 Jan 2026 04:35:20 GMT  
		Size: 34.6 MB (34570247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931f74f5b7466686e473d831087f610a869317f3b9b22f012a1420d1fcae2c0b`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:573f44b42b6286b2c5ea71cc9a2655392f5cb46b7699411496b7b2d330a2dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1384223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6038e714acf6e08ca68b0abee640bb1adb1b1765e3c5485fd2a9a94b38c2c7f`

```dockerfile
```

-	Layers:
	-	`sha256:3c3a055147502d21bc8a0d1b33bdb99c685ea97d0fe1c54619593cb5be523041`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 1.4 MB (1359233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd9432d5b9a2c79ff5fe657ea3c46184778901f28ecad8d6374a72b3cc250a5`  
		Last Modified: Wed, 28 Jan 2026 04:35:18 GMT  
		Size: 25.0 KB (24990 bytes)  
		MIME: application/vnd.in-toto+json
