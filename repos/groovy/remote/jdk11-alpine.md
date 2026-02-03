## `groovy:jdk11-alpine`

```console
$ docker pull groovy@sha256:6a223f88f15a4ed1d32dcbbe4bd5a7effe6aab6565ff61d887b455b0e4826d3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:jdk11-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:281f19b309bf9fc3734ec4add19605df4de23d21a703fe269040b1256809fdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194762577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4cb39c821dfda24c57531209b4619728f4f94dd83579285c3da1526b9d4fc7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

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
# Wed, 28 Jan 2026 04:13:39 GMT
CMD ["groovysh"]
# Wed, 28 Jan 2026 04:13:39 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 28 Jan 2026 04:13:39 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 28 Jan 2026 04:13:39 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 28 Jan 2026 04:13:39 GMT
WORKDIR /home/groovy
# Wed, 28 Jan 2026 04:13:39 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 28 Jan 2026 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 28 Jan 2026 04:13:47 GMT
USER 1000:1000
# Wed, 28 Jan 2026 04:13:48 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
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
	-	`sha256:0dd676b6def18bcbfcc158fd0033c0a632ac48375ec8ea01bd53c053eab49b06`  
		Last Modified: Wed, 28 Jan 2026 04:13:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d7911f3a7806ea2505bbea251abc4ad974a50310aadbca1e0a32f3ffa7c98`  
		Last Modified: Wed, 28 Jan 2026 04:13:56 GMT  
		Size: 34.6 MB (34557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a513726c91bb0b5608d42fb071553a2b5680016fc1c2a25b0ba109af80c59ceb`  
		Last Modified: Wed, 28 Jan 2026 04:13:55 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:153d975fabcb1474bfadc6c1f32f3bd7421f9cebb8d63e56b583863ad5c736fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd5c52d2849ce1e12f14c0d504334b2e8e6e51db384f2adb74c2ea5293dd737`

```dockerfile
```

-	Layers:
	-	`sha256:e73071f589033bb845f12b3a665a6c2fc7a12de6a08d9ede2df4200116ff3b03`  
		Last Modified: Wed, 28 Jan 2026 04:13:56 GMT  
		Size: 1.1 MB (1101826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a92ea562fae7aee671fb19df8af7b8e14047af5bf88bab7337d9b9a70c9ac7f`  
		Last Modified: Wed, 28 Jan 2026 04:13:55 GMT  
		Size: 22.3 KB (22295 bytes)  
		MIME: application/vnd.in-toto+json
