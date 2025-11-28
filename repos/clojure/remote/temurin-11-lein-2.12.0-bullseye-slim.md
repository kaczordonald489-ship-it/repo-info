## `clojure:temurin-11-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:e5c8128e0103e59145544ed79179b17a976804dbd8cfcc6c5e965436a8ad185c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9050a4efdb94ec21356d8ab41a77bfc55c2b575b8feba904f2403d1166183267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195061598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdae068a274bd7527ea9dbe16edeb8f5df21ecd49e8243dc019545868aa555b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:07:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:07:05 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:17 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:19 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2207419dddb167c29d90929006d7657af2addf2aa43de4229d99984fc0418`  
		Last Modified: Tue, 18 Nov 2025 09:55:33 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf345cca5cb433420d4150406a662fa0cd05c1be8028c68e05d5c56c2d1d8e74`  
		Last Modified: Tue, 18 Nov 2025 06:07:52 GMT  
		Size: 15.3 MB (15318721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c668760e44f60d1db95cf2cadfeca60bbf06765bca153e4e2093c2b440a4c4`  
		Last Modified: Tue, 18 Nov 2025 06:07:50 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce9857de2ffa28d437228e924eb91c94a70a8c2ca272794e3438125857663f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ceab9972c5ca18f4585055f9f268cd39ca1cce22e67c80442041ac8ef7e965c`

```dockerfile
```

-	Layers:
	-	`sha256:8dc5341e177121408cea9f866c79cf3d1662dfeb251ccf80963d48b970d7c85a`  
		Last Modified: Tue, 18 Nov 2025 07:38:26 GMT  
		Size: 3.0 MB (3038049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a58497fa3d32524ea1dbb17e9dd24ca073a27fc62444d48564a90ed6627db86`  
		Last Modified: Tue, 18 Nov 2025 07:38:28 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80c5fe3acefcc75116d94b28271460a7c679de4f2d02801cfbb5b40c1bed85e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190303534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855ecd71698d7fc531cf842b2c462ad7cc2d032a70b79dcd1910151667821220`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:48:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:48:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:48:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:48:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 03:48:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:57:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:57:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:57:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:57:15 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:57:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:57:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e409d8923097838e94d274f9d85ef99ab4c5e30630806588f7ded4d05058f870`  
		Last Modified: Tue, 18 Nov 2025 06:51:02 GMT  
		Size: 141.7 MB (141731502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3661f1968d6e27f2013b19cdc9dcb154fe0196490b93f9951864d69c64c58a3`  
		Last Modified: Tue, 18 Nov 2025 04:57:32 GMT  
		Size: 15.3 MB (15305809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489ad45ae5c17aba9915f0b9becaad02d4abb93a2b197c3d7cd6ec3fd0bcd213`  
		Last Modified: Tue, 18 Nov 2025 04:57:31 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64f834bc35cefa71afc713773396113c597471ee2110a02e3d28448c7e1db3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fb8b6e43b9fd716eecc414a6508b9f04512037056a55892dc368bc51b98e95`

```dockerfile
```

-	Layers:
	-	`sha256:56c906bea4e5ff970950d17fc00046f5b71377d4d5cbbb1eb5f603ab28a25748`  
		Last Modified: Tue, 18 Nov 2025 07:38:32 GMT  
		Size: 3.0 MB (3038276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cc2f5482514a82e54ec7199e10fbc10f21ac0d71f0e401cb176c0a299b59c6`  
		Last Modified: Tue, 18 Nov 2025 07:38:33 GMT  
		Size: 15.7 KB (15731 bytes)  
		MIME: application/vnd.in-toto+json
