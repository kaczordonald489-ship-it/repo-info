## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:f0cf7f6d4f3273be30a8208b030435eb4257c2b9c9edb15bf41bd8718eba0657
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:fed22d00a520a70ee850325c53689f2f1ba4a314a66b7b6b76fb2aaf6a9f5800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217649757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b83fdcfd767bf00435646ec01443259cf55558585c5491ed1fe49139c6e411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:08:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:08:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:08:09 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:08:23 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:08:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:08:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:08:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:08:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af355cfa5e42735101850c5ddf5e3db2c780be5db58b593cb19edd3134a4bb`  
		Last Modified: Thu, 20 Nov 2025 03:33:46 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c50f913e14771619cef6c301d51f9f846a81778f6cea01565be83f0610fbbb`  
		Last Modified: Tue, 18 Nov 2025 06:08:52 GMT  
		Size: 19.8 MB (19802866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873f7e54f34cb67db71b109610af8e72855bc7fedea24cdf534eff2b034863a`  
		Last Modified: Tue, 18 Nov 2025 06:08:51 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f446114c5e74e1f129aef214dd2be0eba1dd51b97b08e38d618b3bc118e53e72`  
		Last Modified: Tue, 18 Nov 2025 06:08:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c32efe6a2a38b7099ed4bc673ebe7c10f74b83ec8e1edd972da84be91f87e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff567b83e88c8670b53016a5f6aa9a0d8bff793cfec160cd42bd210007826fe`

```dockerfile
```

-	Layers:
	-	`sha256:dc13cf7a5eff8f91174b9382cda8961fa019dad7b22c7bdcf6c94a7984e8dc8f`  
		Last Modified: Tue, 18 Nov 2025 07:41:14 GMT  
		Size: 4.3 MB (4279836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c64d3f3c8eabaf3cbc95ee6b0816073d829697fa086cd09123eb9f117b6d9b8`  
		Last Modified: Tue, 18 Nov 2025 07:41:15 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35931595c1eeb28a4e6eae8ee857d155dbce52478f18246a38d438bcf39ff48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216189422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee047f080360b0f0fd099c42ca33d8736a2772fa4b8cd753db2f99bb0f9709`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:00:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:00:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:00:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:00:50 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:01:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:01:03 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:01:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:01:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:01:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:01:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d3668e2db51bce474c7b67ef499fc8f66561e8fe5a79c3084c8814e154e54f`  
		Last Modified: Tue, 18 Nov 2025 08:25:25 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446894cae360223f98d0a55c1b2ed92262317e6debf0bb64d696c18fe29f2053`  
		Last Modified: Tue, 18 Nov 2025 05:01:34 GMT  
		Size: 19.6 MB (19632173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d30bba1d25671b7d9f0fce3a066f648f4949747e83737b57a5c8e42ea260e73`  
		Last Modified: Tue, 18 Nov 2025 05:01:34 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0d7cc51fb279b537fd1bad7ccb8dd14e7b6554a3a28b42c6a654d00778925c`  
		Last Modified: Tue, 18 Nov 2025 05:01:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9aad285196941bf8fed41cdc940a044f6d558b28b08199bd9ab8edb3c24a9205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39751b5cc9eace89ec89f2664dc374d435cb56858b5873f2617afbf72a118b69`

```dockerfile
```

-	Layers:
	-	`sha256:f1415237139044593de8b58c01a76d1cfe4810101074014b8eebaa7df8659986`  
		Last Modified: Tue, 18 Nov 2025 07:41:19 GMT  
		Size: 4.3 MB (4279451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069ed3f28411b36e4147c0d9df763d67414a023655acebc95e2fba2beb73c0a5`  
		Last Modified: Tue, 18 Nov 2025 07:41:20 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d1614937adbd737c3d9bca5c45a4ec0a5620d1e836c5285bb3ab4a885aecbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924112ffe5a7f01dbfe3e45f8272db07b9ab01685c0998d8c455c2a7bbc511b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:24:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:24:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:24:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:24:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:24:58 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:25:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:25:39 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:25:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:25:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:25:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:25:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e428deecdff730da5ea1d342a0ee4b8cdcf662138452888ec203cf5f5482e`  
		Last Modified: Tue, 18 Nov 2025 06:26:34 GMT  
		Size: 144.5 MB (144525223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0776632ae45d8f838cb2998158e600eca09fce8c8f2326259ebe278ec692e6`  
		Last Modified: Tue, 18 Nov 2025 06:26:40 GMT  
		Size: 20.0 MB (20021649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083ffb1f0fb23cbd13f3574288d82a373b0f3bf6b831d5c23b056c2278c5e9f`  
		Last Modified: Tue, 18 Nov 2025 06:26:38 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf2a569b4b78ae4b5000b5b16b42e4eb88902f6a2e1244665479d55eb886117`  
		Last Modified: Tue, 18 Nov 2025 06:26:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91a6567243a68f71d3022fc8957384770f085efb2345f061816b5e86474e9e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdb90daff36c73ffd07f606078747ac4f482cbb248825612b33330e7f9f12fe`

```dockerfile
```

-	Layers:
	-	`sha256:b478b867fd4057e65418b54a7688848e146acb42dd474cebacba448444a755ca`  
		Last Modified: Tue, 18 Nov 2025 07:41:24 GMT  
		Size: 4.3 MB (4281695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:750aa449c960ed868f3a73fd54d3410062d869c4e4628b6946d01a1dd10e8fd0`  
		Last Modified: Tue, 18 Nov 2025 07:41:25 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0d7f390e5696542d5d88c1656f790fa4a21316b82919d1d2a551ea5185d34420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205975633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78a313041e8fe24daf54d6dbf6cd85d1487ac794cf726993e0f7cbcbaaef69a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:24:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:24:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:24:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:24:24 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:24:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:24:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:24:35 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:24:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:24:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:24:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:24:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea9989f689694d4dc7b2dd7c0f29123849b9198fb814c834beb91a9c2af71c`  
		Last Modified: Tue, 18 Nov 2025 05:25:05 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21254cdae16e4cd408acb47a31a7974a5b43afb999c50bdc1ac96508f656a72c`  
		Last Modified: Tue, 18 Nov 2025 05:25:12 GMT  
		Size: 19.5 MB (19460760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2683ee40f21287d63718ca4990b1a4e05f755d777cff03f26b2e4449517a9a`  
		Last Modified: Tue, 18 Nov 2025 05:25:11 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb7b637e00cf8631e96aa216a214fb2c8b7af2ea826869ed037904ecad40a3`  
		Last Modified: Tue, 18 Nov 2025 05:25:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a759c3d72b5c562ecd032f7b28ae0c5669c4e86449d678b26adc7d59d7112607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fdd923213a33d35d26cd0785374630be782867f9eed73518098d7cb17948ad`

```dockerfile
```

-	Layers:
	-	`sha256:562bd2ec59b726e0a4de6a99e062e2f749ac459c7e3b8ad4e16053cda16f796a`  
		Last Modified: Tue, 18 Nov 2025 07:41:30 GMT  
		Size: 4.3 MB (4271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4aa54bb6a607742ff1937610b4779451e7238f36c57f65ddb0922590d23a71c`  
		Last Modified: Tue, 18 Nov 2025 07:41:30 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
