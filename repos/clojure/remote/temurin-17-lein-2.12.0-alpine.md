## `clojure:temurin-17-lein-2.12.0-alpine`

```console
$ docker pull clojure@sha256:57240c42d0acb1a213b8317955af542c92f3d9a95f4db4f7ade4592400b5f63f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:518a7bdae06c52603b5182acb768e4b53e06d026f87b5a33ef2ea0730cda4de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188306315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffddec98dfc410ba483c49854f081da59bb2bfa6e35654f7355fa3679c3ecabf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 28 Jan 2026 04:25:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 28 Jan 2026 04:25:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 28 Jan 2026 04:25:34 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 04:25:39 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg # buildkit
# Wed, 28 Jan 2026 04:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Jan 2026 04:25:39 GMT
ENV LEIN_ROOT=1
# Wed, 28 Jan 2026 04:25:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 28 Jan 2026 04:25:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 04:25:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 04:25:41 GMT
CMD ["repl"]
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
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd6195651db15e627aeee8f9dc9bf7b0da4a5fada50c7f1c093d04b68c4cd5b`  
		Last Modified: Wed, 28 Jan 2026 04:25:48 GMT  
		Size: 14.9 MB (14875921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda09e6f2f4ea2815baadfe2c65d519f2dbf190d5e3cf56c42c3e8be8e5c5546`  
		Last Modified: Wed, 28 Jan 2026 04:25:48 GMT  
		Size: 4.5 MB (4517694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b097c6891a49df6ac5777f59cfeb0a45f0d6e0f9d02a826e29078850d6736c`  
		Last Modified: Wed, 28 Jan 2026 04:25:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:9d409a609fbdb8ba50187e3cdd98e7b5778a97b7cbae95fad21dcbd7e9d6e95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1075626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04409fcee4e26d3854c23ddf3b990b0ebf473bb5255232ee4ba4b6409260113a`

```dockerfile
```

-	Layers:
	-	`sha256:ae892c7148da8c3ca796037ea4adcb10d0c1528093a0b8a59509da397d6ef390`  
		Last Modified: Wed, 28 Jan 2026 04:25:48 GMT  
		Size: 1.1 MB (1057412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37457748f66dfef26aee9cbfdda1cbf62dd1d0f0031d313eb9217c8b9ece06a5`  
		Last Modified: Wed, 28 Jan 2026 04:25:47 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
