## `clojure:temurin-25-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:34e4096ac7eb1f8c1328766ecb5a5fda2fcbc5982226ed505b7eb2744cf3e76c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5c8f5c02e481315f374c44ea4c0848610be62fe5a3791ab14c5e8f90c9863048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166927393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e85446d69778bf6e06f75bd28aedda22154484c99c49b92bd94cbbb4a5ca81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:36 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5323c0bf9775bf552591545178e770fd9cbad7a81252527896e187c93cbd24`  
		Last Modified: Tue, 03 Feb 2026 03:23:10 GMT  
		Size: 92.0 MB (92045330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc73dac431ae6fbb5b30dbfd476a77e670913b66b2a15b7ec687f9fc37d8239`  
		Last Modified: Tue, 03 Feb 2026 03:23:00 GMT  
		Size: 16.6 MB (16607623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ddfe4ff6417cd38883a424f07d63e40db066b89ce84f7a08b5d1bf27e092a`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca1840ab7bcd9455f2d36aff3a0cfc3508dceaebb89e11b87bf1b1dd1bb383`  
		Last Modified: Tue, 03 Feb 2026 03:22:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e4479ba8feef7b3ea946a3daf612da484761fb857b4c3fa1b678ffd7a42956c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afd679c4aebf19f852f2b946b034a26fe0ab94b83b8661f3ce297c0744402e7`

```dockerfile
```

-	Layers:
	-	`sha256:1088b14ebdf28c7b0841ac11b744381ba5e46b833d3789a7831b7f73c197827e`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 4.4 MB (4427494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c05ff1ce33f190370c5f929e5d58da041d1310e9acf98a04c869d57842ec05`  
		Last Modified: Tue, 03 Feb 2026 03:22:55 GMT  
		Size: 19.0 KB (19001 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3c8fe2b67588520c8015bb6c4004ce4149a0ca7d0cab1130be6390954a523dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164424008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdbd820a697cb5dc9690e91a0db548eea24ead5c2375ca1477b4b4d065b6446`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:24:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:24:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:49 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:25:03 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:25:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:25:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1181a9877b53aba3ec05e495663e8b02bbb2f3b988de81ff91d7821416af3`  
		Last Modified: Tue, 03 Feb 2026 03:25:24 GMT  
		Size: 91.1 MB (91052475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa069a65cd16c244f11bfabe6562a76dc34eac5581256e57337dd481365647a7`  
		Last Modified: Tue, 03 Feb 2026 03:25:23 GMT  
		Size: 16.6 MB (16595033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636e3a20ae47d9dff1207f6f0bad37f3699e8349ec6adc4d65accff5f373251`  
		Last Modified: Tue, 03 Feb 2026 03:25:22 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ad67dcb5fe7b4c995f1b388b0e2eeb4953284fac7409c05ade93a2a1cc2a77`  
		Last Modified: Tue, 03 Feb 2026 03:25:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:97fe6da9bc48a84d0dff82ac88856f9ce6a8f7ecb60d1b1393389d8f664cc9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bdfad6e919456f007d708300da52484d1c8c623297f3fddb2588957a7a205f`

```dockerfile
```

-	Layers:
	-	`sha256:a3cc795e865126014c1548de0f8e72ad0415165b5a3718ea75501c078877fb83`  
		Last Modified: Tue, 03 Feb 2026 03:25:22 GMT  
		Size: 4.4 MB (4426489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192194fc0747ffdc6f2affcbfe708c4c6eb43c5f0ddf47a395877ffdd5701856`  
		Last Modified: Tue, 03 Feb 2026 03:25:22 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
