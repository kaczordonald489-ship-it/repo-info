## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:be4b50ef86edd60281b1006292203f7c006a5eee35e237cf2f6b86865aa5f237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d127dc35214b7df561f27721b25a08fced1a6c8b4d659d3acaaaa351569edcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195589726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c0563e5b98f08a1dd8b589dc844fd8e8bcbd9191439a8c66d2b4dc1b3ca5f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 07:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 07:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 07:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 07:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 07:19:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 07:19:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 07:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 07:19:17 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 07:19:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 07:19:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 07:19:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 07:19:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b725b2ce4d23bfae010846db960a0a92356283b2181fcb858a1d725003aec5`  
		Last Modified: Tue, 18 Nov 2025 17:49:19 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b8ba4c960ec6a6bb0972a06c22a3f05330ec8679ca97f7d4c1bb62111098d6`  
		Last Modified: Tue, 18 Nov 2025 07:19:45 GMT  
		Size: 16.4 MB (16447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2051ab1ee72597ca53c9442346145e6168dfbfff1ba7ca3570c022aebde6f4`  
		Last Modified: Tue, 18 Nov 2025 07:19:45 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd844744497c0ac17d2f3edcaf2b72d8c3dc01bb794c02eff1a63e71ce624e`  
		Last Modified: Tue, 18 Nov 2025 07:19:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ba7ec06145d805560cf95cdbc552ac6cb9111c66d3b6680876ec01b6e291c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe3cb9f536093397abe84c7fd5a73146b2dfca710aa3ac63e6f1029d5d53f03`

```dockerfile
```

-	Layers:
	-	`sha256:45c0d0e943e9d7a3083496075ec21989787102b5620f65a50bf658bf4a912442`  
		Last Modified: Wed, 19 Nov 2025 04:35:18 GMT  
		Size: 2.4 MB (2363438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e232a11f619b893b6cedcbb40bf35c7b61b8aafbbd8f48d22d8798cf13f3f14d`  
		Last Modified: Wed, 19 Nov 2025 04:35:19 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e88b7f3fcec02f8eb85aa06c599b1dfcb724ae0bb1709abbe04de6beee8c27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194750535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f433c45d1950538a2b5c8da4f448316ceaee2b4f9f949bb7c6c4cf18b4a20ee1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:03:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:03:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:03:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:03:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:03:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:03:36 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:03:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:03:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:03:52 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:03:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:03:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:03:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:03:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e0f4b0d34c396fd43277f47df439be4d0bf3761c949fcabb8ebffe7d0a6243`  
		Last Modified: Wed, 19 Nov 2025 14:18:05 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134ab81aeb983dc89d857aeac255cd15250f2aca54b8d2d94abdecf40fad7f23`  
		Last Modified: Tue, 18 Nov 2025 05:04:25 GMT  
		Size: 16.4 MB (16413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14639dc9fd4dfce0f4efde5c8f54afd87d415f708bf795c66e1ec4f7ed41d8b7`  
		Last Modified: Tue, 18 Nov 2025 05:04:21 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deabc8d38f8a64d4af03a49f8a3f9784c7fc2c3324b1ed9e23cb51b106726ac`  
		Last Modified: Tue, 18 Nov 2025 05:04:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86d3c1522970476e2e90268ed78ab017ffc3623430e52dbc179434482c14e180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f9427fab626441d9694d173869ff35dd06b3c2fce68c5a20ad62ff5a5d2623`

```dockerfile
```

-	Layers:
	-	`sha256:1379d227d6a8a41c3001dfe58098a537597e787d01e87ddd47ea856891943bef`  
		Last Modified: Tue, 18 Nov 2025 07:42:14 GMT  
		Size: 2.4 MB (2363056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d6e18918cd54fe74ceb241b9c23705bdbf12fe365cf3d6d20551ef5035159f`  
		Last Modified: Tue, 18 Nov 2025 07:42:14 GMT  
		Size: 18.5 KB (18507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41141e825e660c462752bfe70f8e6c8d0805aed28e93b5aac9a44e82ac76e183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199125407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fb1a41413cc2ece9a1bc061008e8c6c1aa6fe8bd84ba20d4bb427ba649be7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:18:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:18:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 19 Nov 2025 01:18:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 19 Nov 2025 01:18:07 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:18:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 19 Nov 2025 01:18:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 19 Nov 2025 01:18:43 GMT
ENV LEIN_ROOT=1
# Wed, 19 Nov 2025 01:18:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 19 Nov 2025 01:18:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:18:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:18:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265887b1da4e953ccb001f192116d1c869d3152ace48f57d173138e0502273d`  
		Last Modified: Mon, 24 Nov 2025 10:02:24 GMT  
		Size: 144.5 MB (144525202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64652aa2c01f5a2b33f273150b08b2828349032bd17cb7d1893047b34f776321`  
		Last Modified: Wed, 19 Nov 2025 01:20:04 GMT  
		Size: 16.5 MB (16485202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015d2403e9c05b234b7aa9577563cda555110988c49b8675f67da564c1f86412`  
		Last Modified: Wed, 19 Nov 2025 01:20:02 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcb7359edfefc440d5e37a907d3734e70dbd484ef7d021ddc90c6b572aa3cd0`  
		Last Modified: Wed, 19 Nov 2025 01:20:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a295a152844634e3553975ff80771b13b939e8261a88761663084c880010c0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d8ff6ca065c6cf36556bd0233bc0a8caf136f0e26930b62572ff2024d15fc6`

```dockerfile
```

-	Layers:
	-	`sha256:d928925d2fb4465f7644ab3b9c94ea5355d9764039222209c2755fb2d44580cb`  
		Last Modified: Wed, 19 Nov 2025 04:35:25 GMT  
		Size: 2.4 MB (2364418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb251b7a9b75870a368852549f785014d4d8d29076c74a91785695875755c047`  
		Last Modified: Wed, 19 Nov 2025 04:35:26 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b1a80a8117dc04fc5be6c5eef6fd975dfe5272451b345a44d5d58c3d7419093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191078777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b0e21464a7df63ca6d4417591b1f14e574806c96de1ca0e62b7ddb4fd1b46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:58:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 17:58:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 17:58:06 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 17:59:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 17:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 17:59:34 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 17:59:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 17:59:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 17:59:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 17:59:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d74684f217d805ec7013972d089a9baa3e158cc8603592f0e9ad77ff195488`  
		Last Modified: Mon, 24 Nov 2025 10:03:10 GMT  
		Size: 141.9 MB (141889576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d70e98f969d860109ed6f2ecfd566bc9476ba24cd78021946b677638e57e1`  
		Last Modified: Thu, 20 Nov 2025 18:03:51 GMT  
		Size: 16.4 MB (16397848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd61d43029dfc2e57a4c10d9515b742a50cd51f77d8bc2ddbb17a069710a6313`  
		Last Modified: Thu, 20 Nov 2025 18:03:57 GMT  
		Size: 4.5 MB (4517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c772892cded581cae2d9cb440de63a40ab8556113e3ebd34662454a71abca3f5`  
		Last Modified: Thu, 20 Nov 2025 18:03:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7148ceca45478fb8e7a07ce85b52370be491f39de7a808d77e0f7cb49855d628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c030b9005fda5df9d1a153ae5aaab64374dd55d3f462bbed93cf56ee7d767fd6`

```dockerfile
```

-	Layers:
	-	`sha256:6eec10e416a7770b0f8ec56a30e004ea476567022090a7b02aff9a7634d9bc19`  
		Last Modified: Thu, 20 Nov 2025 19:35:40 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d8fe1d817dfcfc7e2352cff1ea6c92f28741ecba5347aacb9633519a4604f9`  
		Last Modified: Thu, 20 Nov 2025 19:35:41 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0276913ee8b77121f0e91ae6b73b871cd2f6b4980147db67d945cd5634bc0c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185694634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe1a7b8b268801ecf9a86e5ed45b80fcdc0b7d468dd91e7548938b0a5e5e861`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:25:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:25:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:25:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:25:47 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:26:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:26:01 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:26:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:26:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:26:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:26:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd69505e1c59ef5e3e9f342213f7e27856756357d6e5b12c0521b80829ba4e28`  
		Last Modified: Tue, 18 Nov 2025 05:26:34 GMT  
		Size: 134.9 MB (134859067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b8b0910a062c137e8efe2e02eca693074f52cbea072c1d6abce1acb4bb093a`  
		Last Modified: Tue, 18 Nov 2025 05:26:39 GMT  
		Size: 16.5 MB (16483014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ab52df7fd5e3202aebaf150028466271aa0f3de937107e706b958464a34a1`  
		Last Modified: Tue, 18 Nov 2025 05:26:38 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bdb95bd1a609850d91f3eb4d1ed2c985fc94757e9d4c1094ad01c1662e2844`  
		Last Modified: Tue, 18 Nov 2025 05:26:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56e027f18981333836fdbf43c263f799ef5a0bf59854d6c07193af7912f316e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee42977da6921a6bd6ab68056bd58568270da85765463a868a4165a16398b06`

```dockerfile
```

-	Layers:
	-	`sha256:95fb7ef0a148a56ef15364b8bd5e024be2cebfd26909db3668bd5fb71a3c4e82`  
		Last Modified: Tue, 18 Nov 2025 07:42:24 GMT  
		Size: 2.4 MB (2359865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a33f3439364e95a32d3d9fb2c3a00eba891bb7082b074e73459004aa5c9cc45b`  
		Last Modified: Tue, 18 Nov 2025 07:42:25 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
