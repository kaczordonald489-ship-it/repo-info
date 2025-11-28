## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:db05e7e41e1333d9446c66b035fe49eae6a76cdab651872101d8388f5e7b45ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e4ae08be42113f76039540f96e756eda2578fbb7a2d14adb855a67febbef5821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195352644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036e57a71b4298eb43cf1f4993cd1e3708e183de2c7dd3a69a5b8f5fc45d279d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:08:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:08:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:08:12 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:08:25 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:08:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:08:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:08:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:08:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427d6d9a9bf953bc78b43d791bcf8e7f1e207ba8589390aad489bd3dc372c051`  
		Last Modified: Tue, 18 Nov 2025 09:55:53 GMT  
		Size: 144.8 MB (144847950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab3a3d7be2945254bae7a2b3462d796a8f0ae0e099e151f9c8fa47ba7661fe4`  
		Last Modified: Tue, 18 Nov 2025 06:08:53 GMT  
		Size: 17.8 MB (17758067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c618b12c843d7b67919ba196bbc4d46350ef7700f6e9cd5e25db20f2af2d699`  
		Last Modified: Tue, 18 Nov 2025 06:08:51 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1710298113a2fee9f0ede27d4d3b10505dfa31f8b267a6eeaa72bb7143f5f85`  
		Last Modified: Tue, 18 Nov 2025 06:08:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:586b057610f6b98590c1f944385bf806fd0b6b453d28345a14c3e0168e283230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15da609474f34e60b37778d6c917c463354369be700169a7e614b58ffcd7429d`

```dockerfile
```

-	Layers:
	-	`sha256:73b1446fa318dc495f9d4a380457293b51910e04bbef086e4c006ba1783475b2`  
		Last Modified: Tue, 18 Nov 2025 07:41:31 GMT  
		Size: 2.7 MB (2728788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d5035f88f3ac5b94071b50797aaca3d8f98b94590e765565dd403a55997703`  
		Last Modified: Tue, 18 Nov 2025 07:41:32 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfed0320ed8c1009117bd98598ded2bdfc4e4c6e21859a1a3f96ed1ed72fb74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193891404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965bab2376fed6739183a2bbddf1f185831e84dc6aa5ac3c7460d9b1480b50e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:01:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:01:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:01:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:01:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:01:20 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:01:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:01:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:01:34 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:01:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:01:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:01:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:01:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f612363b4dbfe909563ce5ee97fdc22ff2865daa8075478a5dd7cb598aea618`  
		Last Modified: Thu, 20 Nov 2025 20:14:05 GMT  
		Size: 143.7 MB (143679886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af2777868c42bfe0d801f52cdb8b2e231ac840ed1b130906b3ff48430fcf66`  
		Last Modified: Tue, 18 Nov 2025 05:02:01 GMT  
		Size: 17.6 MB (17591136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f4e03d298740defda20a085ff1edd4b75470ede5c6d8e616c1e035dea4d84`  
		Last Modified: Tue, 18 Nov 2025 05:02:01 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c2f156b6c8dc0c6812f68ab8243a59b0778086b1ead6d1e58035148f8cf59`  
		Last Modified: Tue, 18 Nov 2025 05:02:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5920bdb5c440671f60bd5bf4d32090128d23d701a13616dbb48b858e582b267f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28dcc1747dadd270e16d3580827b9e997f82d2beee02bb8c03a2f4890d1f67a`

```dockerfile
```

-	Layers:
	-	`sha256:7ce117b142b0470c0dffaa375c29dd3e8f959f62b7379513e3f199cebf3f2385`  
		Last Modified: Tue, 18 Nov 2025 07:41:36 GMT  
		Size: 2.7 MB (2728403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224cc8a6430c5c644fed8c3004bee87984c75ed2fb6ef818fe4975571cebf91a`  
		Last Modified: Tue, 18 Nov 2025 07:41:37 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6c319c0eaff5343ae49a5acce8c3d1359af4e5cbad05ed53cf20e0c6fc10c1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a058cd8d85094b47f5759e48f0681d210044487750ee0cc7f6c433d61d9d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:27:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:27:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:27:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:27:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:27:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:27:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:28:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:28:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:28:00 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:28:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:28:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:28:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:28:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172e760286a339898f9ca04793550c307642085dbffc819262542c00d0caf079`  
		Last Modified: Tue, 18 Nov 2025 06:28:44 GMT  
		Size: 144.5 MB (144525254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2d7226cb1dbbef24d36b65cdcc135cf28deb3496f2513923389d59370de4b`  
		Last Modified: Tue, 18 Nov 2025 06:28:51 GMT  
		Size: 18.0 MB (17959654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c94d97d31da75c6426b3e4242f7202ef509ca698598189f3cd331eca7449d9a`  
		Last Modified: Tue, 18 Nov 2025 06:28:50 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc9cc14ef4a5c3f357ccd25652c3e0bfe6fd512647ed3fd2ded8d49b2bf2334`  
		Last Modified: Tue, 18 Nov 2025 06:28:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f024806172d1cf18158c84708290c74d7b61a0e0bc97d983820bc15a1c849e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a25d758102fbb7bb457caf3c131df57595634c1ae1df397d7a5f68c99711f53`

```dockerfile
```

-	Layers:
	-	`sha256:96108558e392c2991e5a507241718467c482545dbdb9df0774091e68563bb973`  
		Last Modified: Tue, 18 Nov 2025 07:41:41 GMT  
		Size: 2.7 MB (2730621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb45a10d7b0ff409d20d0c32682dd214af2c3194dadeec26ba74365d732ae7bd`  
		Last Modified: Tue, 18 Nov 2025 07:41:42 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:83c2709130a5d817ef17a1440ebd2c2ccddd5d84608a6266e9fb36811bb28b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183681398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d343b06cb73a9f88589f01eedaf3f981dd23bd9fd429c019eca4c9f6cc7a39f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:25:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:25:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:25:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:25:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:25:49 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:26:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:26:02 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:26:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:26:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:26:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:26:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a11b9c90e42947d63125b1586252482ff242a7c5ee2cff882824559dda83f`  
		Last Modified: Tue, 18 Nov 2025 05:26:37 GMT  
		Size: 134.9 MB (134859061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8097bf7fd8891936150e18210b02dceebd3d2af5b10f025f535e71ac5da05f3d`  
		Last Modified: Tue, 18 Nov 2025 05:26:47 GMT  
		Size: 17.4 MB (17419772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a45d75e137414acc0c4e0b170d4d47de596f09ac9a73e2ed5b7b11629fcf3f`  
		Last Modified: Tue, 18 Nov 2025 05:26:45 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27797b288530218d844fef5ed6c8886521bfd2465838e9a6449abded9fd006`  
		Last Modified: Tue, 18 Nov 2025 05:26:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfb8c701db86fcf7f2007c425574f591663e63c9390d40d77eb738153d4a25b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438c7e315a31eff3c21b1a0fac3bc89d5b0c73c54a57e74093e10fe5de10779f`

```dockerfile
```

-	Layers:
	-	`sha256:e90a4a34a9765d87b11d6b32ba9534c03197971da36601c58ba26eeefe19c524`  
		Last Modified: Tue, 18 Nov 2025 07:41:46 GMT  
		Size: 2.7 MB (2720602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3ba170e29056b6ad17f58203bd897a3e6f64599f1994c0e912d7c3f60c59d0`  
		Last Modified: Tue, 18 Nov 2025 07:41:46 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
