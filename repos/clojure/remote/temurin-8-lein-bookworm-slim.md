## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:70e4e75b1fafb1f50ed65e52cd30bca31484d20f19181a8ec0f4ad1f10f41737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46d9ab8addb8c7a720dc8def5d7b31a0ed7829e3d25eefc5cb8a4c8e455a20d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105237651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc0dad178913d6b782e899338a895c82a19251cf1a11466b9381b7f1e92f0dd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:04:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:04:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:04:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:04:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:04:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:04:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:04:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:04:42 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:04:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:04:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee59f39d2df1e6d3529baf5ff2d7ca2e117fa1892934a10c54f3bd470fbda48`  
		Last Modified: Tue, 18 Nov 2025 06:05:09 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9866688a4c8ff3176552fadc0cb6628f72c4b9bd56386cb379cd07cc1579ad9c`  
		Last Modified: Tue, 18 Nov 2025 06:05:05 GMT  
		Size: 17.8 MB (17758049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a550faf3002fd3c3b55e8dfeecfb0a28d458838b21ce4b0e726216ccc68e22`  
		Last Modified: Tue, 18 Nov 2025 06:05:04 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91138ad74e6a717cd95831e588611271ec8b67e4ead3119032c8c5ea9ba13387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712990410685f97fdc5d720ca022ac6e087d2bbf8f8a82416290f2cab373de6`

```dockerfile
```

-	Layers:
	-	`sha256:719485440b844a1eb7e6901bcb22fe1c4c2870abc3d90fb932892e6759ae3a30`  
		Last Modified: Tue, 18 Nov 2025 07:50:10 GMT  
		Size: 2.9 MB (2850398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe25c01ec6e46d23552bc7cfec7913195558399f0d0c1d78b0e6cfb01010a13`  
		Last Modified: Tue, 18 Nov 2025 07:50:11 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:653947cbf70cc43c6257d0a9a54dab8b8e0bf1c1c21686d45df0dc3adffbde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104026100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139f5438b44969e54151d8488bbd482b75bdfdb6b36b5e52d4b0da061ab04f3f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:50:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:50:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:50:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:50:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:50:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:50:21 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:50:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:50:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:50:34 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:50:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:50:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5446494e6b53fbbde6857a540d89f36b09c22954527bb6ecb4555e434d892325`  
		Last Modified: Tue, 18 Nov 2025 04:51:02 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7a58c72e5f4ec942426f633310e0e446dbaff491a120b194f4c4931935443`  
		Last Modified: Tue, 18 Nov 2025 04:50:57 GMT  
		Size: 17.6 MB (17591116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7c4f9bee796fbce46abeaaebb9b0a30d611514625e1b9e010d4696e1b8d83`  
		Last Modified: Tue, 18 Nov 2025 04:50:56 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86459120cc59945ef05d08bc01c891fa65decac52f68f048a32f506e0784bc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da12cb0c2e5223ac9d8ae4084ab33cb627e6218f4930ce543245b55884b45907`

```dockerfile
```

-	Layers:
	-	`sha256:4da64ac9f8c15be8bd3e624e464393a4a598b18263582750b8eed9542ef66131`  
		Last Modified: Tue, 18 Nov 2025 07:50:15 GMT  
		Size: 2.9 MB (2850711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94813833e5eaa6ac3a376c9a156b63201306c4f3375f00b1455d22aa32d5507e`  
		Last Modified: Tue, 18 Nov 2025 07:50:15 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6d35f7fcf84177eff56ded3a5f22d9bed922e03515ebf6122a8fec5e36c0c883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106721364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24353e6734c8e4c985ccd61d20221391b4bad69ed5a8e109ccefc13014063d28`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:14:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:14:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:14:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:14:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:14:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:14:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:14:53 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:14:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:14:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d016d9e912cb735827e82c51514523b6941a4ca5114f7db6b8ad862763e4a5`  
		Last Modified: Tue, 18 Nov 2025 06:15:45 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81f9c179b8e9c7bd40ed5dd38d17cf6beddff67808328f5a033a16ea705da6`  
		Last Modified: Tue, 18 Nov 2025 06:15:42 GMT  
		Size: 18.0 MB (17959599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e15adfaa8f41f23cc54ab171170a36fe1f4f7145d7ec3ea187986185f7984d`  
		Last Modified: Tue, 18 Nov 2025 06:15:41 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b5c029656385604661a788d6d47d6a68aa03d9cb80d9ddbe23adc31a653133e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff34fcbaa429e19fcb861e21856dad279ae738b955d9fa30d503dda495711aee`

```dockerfile
```

-	Layers:
	-	`sha256:7426c330e624c78b1b32dc3fc7e920271abff4ac90f850c6cf6099ecf036c04c`  
		Last Modified: Tue, 18 Nov 2025 07:50:19 GMT  
		Size: 2.9 MB (2852824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46b555e0b6561cc8e5e75530ed2fa093179ce9d7ac71fc12d924f195085b91b`  
		Last Modified: Tue, 18 Nov 2025 07:50:20 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
