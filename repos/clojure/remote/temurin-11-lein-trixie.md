## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:25d0a8c759bd6a21ab3515b1115a60e9d8c6d8fb4b43626b2b2ad20fd817435b
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:96fd5f21ca9aed8142cfd7dbace27d04a15572e8c3b04d008f02683db7e5d959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217353536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b0b45abe3f6b9605dfb82634cd328632abb768fbf869e44c9a4efbf7c5934a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
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
# Tue, 18 Nov 2025 06:07:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78db572841c71d3caa4f2f83b9f2b45604205a8b3e39ae88855a8a0b564f22d`  
		Last Modified: Thu, 20 Nov 2025 03:07:13 GMT  
		Size: 145.0 MB (144966633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9080a978362ad9aeecfd11ce702b8c5c2eaa2a0f677670ff1347f21733b568dd`  
		Last Modified: Tue, 18 Nov 2025 06:07:46 GMT  
		Size: 18.6 MB (18579558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef769b0213a43490df9a51c8ec36eff785349a0649dc83410a6f4da6d396ddd1`  
		Last Modified: Tue, 18 Nov 2025 06:07:45 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d5f665b80859745f9d72b7942052f0ff22ba22bc7fcfa93bbabdb4ccef19fd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb87748f584edfff28033f37a6618df5ff228ca280b150902c3a9e355b0185c`

```dockerfile
```

-	Layers:
	-	`sha256:df6468fce8302a9ee8a185048de1738d050763aa843d3739e0e7e3e7a24e3bb2`  
		Last Modified: Tue, 18 Nov 2025 07:38:40 GMT  
		Size: 3.8 MB (3833519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab3ffec72957a3008565c997838ca96077ba21a4d3fd957f3c90521898e0518`  
		Last Modified: Tue, 18 Nov 2025 07:38:41 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89faec196055a874139a1de55164cc9f3bd443e8ab04ac562242b9d24729beca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214440211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d61af1c2d6d4a3917a614c121eb19e0bf2b4cbcc56866f618c5388351ddf710`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:57:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:57:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:57:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:57:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:57:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:57:14 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:57:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:57:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:57:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:57:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11712c78fc976f496c6d9ee6d0d34f5c2b5b76604ed90999d8eaf1fe2c19593`  
		Last Modified: Thu, 20 Nov 2025 21:31:56 GMT  
		Size: 141.7 MB (141731579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0108a1ede633874996c92138e8a8edfb2f5ac0cde59ded7ba46205017c77391`  
		Last Modified: Tue, 18 Nov 2025 04:58:02 GMT  
		Size: 18.5 MB (18540655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690ae51cb282a4b9bd4f1a1f433058b5b219ddfd0cbdf5d169614f631e4b3b1b`  
		Last Modified: Tue, 18 Nov 2025 04:58:00 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7546bbabf56d311a732c40215d937c57d637898b925905e74bb841070314c06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0bddf0ae7d9ed5f67b0c048b95445e90c15b352fc5c1caa41bb23a9f2ac2e8`

```dockerfile
```

-	Layers:
	-	`sha256:23908bcc9ceaf9206cd77abd4596f0272c57f678964cfdf9c3c0707911095376`  
		Last Modified: Tue, 18 Nov 2025 07:38:46 GMT  
		Size: 3.8 MB (3835014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd25d1a3b8037e43b38b94c5c21e765c96f2cbadfb40123cf7cd4b3a6a5e3e71`  
		Last Modified: Tue, 18 Nov 2025 07:38:46 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:406edf32cd20a1e14d1540ddd61ac6e54487f30b8e9ecc0fc343c0133dd447ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208345390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049b685189540c4754f7fef46e1973853ae90584038027b10b320aa0112fcfbe`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:20:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:20:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:20:28 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:21:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:21:14 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:21:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:21:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb45d70f1a9cc9b98db4aadb38d046c09df2cfca82e5e26482a0ddb0592166f`  
		Last Modified: Tue, 18 Nov 2025 06:21:41 GMT  
		Size: 132.1 MB (132081977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2f650f0eee94f925796400b8ffd98a35bb8bd2d71faf46a7e9229eac064f1`  
		Last Modified: Tue, 18 Nov 2025 06:21:58 GMT  
		Size: 18.6 MB (18637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c73aa7ffa0c81cb9187edc2a0c94824428b1d8eb0d4b819c9f6313691805b8`  
		Last Modified: Tue, 18 Nov 2025 06:21:57 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb6ad6bf55ca993095acadc000ea6421391dd009e4355b0aa825f98323f4b9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bc055aac6ad4b59156f4a763e7a98238feab08330a98cd9ca7d54adb6f1f76`

```dockerfile
```

-	Layers:
	-	`sha256:d9ec6dce9bc5ccb9e5bcd2bd369882dcea728fded14ff6636e63ba6a1aca4198`  
		Last Modified: Tue, 18 Nov 2025 07:38:50 GMT  
		Size: 3.8 MB (3833902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f2cfd6f08e80db2bac4e286dfe21ddac3ea5777ac261166eb143871ca9f683`  
		Last Modified: Tue, 18 Nov 2025 07:38:51 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5e9748cbde7baab8298d4ea2927db6aac22bf043a596b166bf1d5855720ab441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33413a1ad8e9c97fe9bf48e46a48317342c411c3a5db540de78a52ebede1215a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:22:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:22:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:22:44 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:22:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:22:56 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:22:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:22:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a70cb1c823d5e23b35944c88065c13443837da05f853837830e64a9332d56c`  
		Last Modified: Tue, 18 Nov 2025 05:23:40 GMT  
		Size: 125.7 MB (125694435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd8cedce4a4925458bd493ae3937ecd3dcc3df9376f754aa9dc92cae1f7fe7`  
		Last Modified: Tue, 18 Nov 2025 05:23:31 GMT  
		Size: 18.6 MB (18620576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7909e65bd9bcaa9aa24ce44063bcd27707a4b01f15bed8405aef2c370cf2b851`  
		Last Modified: Tue, 18 Nov 2025 05:23:30 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:248f2111f33c3d56e73f79f7eaf6b5182070c4d0cb4fd5c925ca5a6447d3f3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19764231282fa133314abefc3d1b0f71e7601192db0093dc18c5526d7595fe6f`

```dockerfile
```

-	Layers:
	-	`sha256:7e4b1f031f8351bfe655a17bde0343c7dcd8dd2bdec9ca21ee893b52227bc006`  
		Last Modified: Tue, 18 Nov 2025 07:38:56 GMT  
		Size: 3.8 MB (3829950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a689f43ecbc6a7e63b1767ccf5b8d6156a83e51ebe49914e89668d23eadf6bf`  
		Last Modified: Tue, 18 Nov 2025 07:38:56 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
