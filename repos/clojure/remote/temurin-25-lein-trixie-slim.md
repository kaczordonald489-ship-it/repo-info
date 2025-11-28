## `clojure:temurin-25-lein-trixie-slim`

```console
$ docker pull clojure@sha256:f54a8fb734e20995ad55ac3cc818a6f7501c157bf57f050052d205bd629b733c
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

### `clojure:temurin-25-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1909f97198f490d405b69ca33476e55e132169519c3352f34ac102af69f081bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142787025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4c36b5dd1b616f450ba1f5cf8892e22dca76a6cb40d9d79210ef81202e21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:16:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:16:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:16:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:16:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:16:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:16:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:17:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:17:03 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:17:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:17:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:17:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786d304fd08ff1992af1ed85286f3c17d938d58f92533cc587bfdc20b3bd794`  
		Last Modified: Tue, 18 Nov 2025 06:17:34 GMT  
		Size: 92.0 MB (92045299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a4e0d87cc2e63313cc9f06fdc096e0ec24ae5c43a70da55bc7473b13a79433`  
		Last Modified: Tue, 18 Nov 2025 06:17:30 GMT  
		Size: 16.4 MB (16447101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8083125c32ed342b1e8c8d3b13c1920e8c6b162a3dd7a8f10a1c2758a3686a6`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb597ad660a179dd9f19c4a929f9b3e2c4ea80e65d571d15226613422caa2d2a`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60821d8bb0e285bb09b56957741007ceb7824ab9d5ac71c0d356aed450218729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a9a2ef978a6c9407b82390199c569e90e1d372cf9b287aeb8762f869ca6008`

```dockerfile
```

-	Layers:
	-	`sha256:0b8f4873b1ad5b7a2aa69af57313225576dafec12f67f694d89f6b1dcf3788c5`  
		Last Modified: Tue, 18 Nov 2025 07:36:44 GMT  
		Size: 2.3 MB (2314754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3917291c110e96694fe801523d5dc73b5db94d070d6c505ee2e38f034bcf5a3`  
		Last Modified: Tue, 18 Nov 2025 07:36:44 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d21542fb30af653df13ddfb1f2c4f4e90a95576d3d8a6a43bfb757ad3f438f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142123129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b30b2e72221b62bba8204419471103affd8eb1c7fe0358cf9f7f2f4534e543`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:14:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:14:15 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:14:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:14:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:14:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:14:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:14:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:14:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:14:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20866dcd073708566ec12af37589b3f1cb176987b8f515b477ec12f7a31934`  
		Last Modified: Tue, 18 Nov 2025 05:15:13 GMT  
		Size: 91.1 MB (91052500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5cf42407a5c26f09a49046f2c0a3f96db99989f96830750e7ba09e0ef750a5`  
		Last Modified: Tue, 18 Nov 2025 05:15:02 GMT  
		Size: 16.4 MB (16413846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb6e9368f6d335ba0141e1a1268affc5c99044056c008eacc6fd6aee4f18b5`  
		Last Modified: Tue, 18 Nov 2025 05:15:01 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622709db5333f8bdcb9b960f3b37e0a433d2d599428e8fe6750f6bda51426e03`  
		Last Modified: Tue, 18 Nov 2025 05:15:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7516dd082dc99934866c7f7ac78fed607ba472a388b428e59bcc25cf62eb7552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca2ce2054d0e6d9a81f78adcbaaefa514a1513571d8320269e2a2b025392983`

```dockerfile
```

-	Layers:
	-	`sha256:42a231dd18b3aa05c17a9eca5d7ed9f205f514b56fe99669a877ea323cc3d559`  
		Last Modified: Tue, 18 Nov 2025 07:36:48 GMT  
		Size: 2.3 MB (2314393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa5ae65d408ebaafa870861aeb1118849e126c791004dc03e58cb6d2d18642d`  
		Last Modified: Tue, 18 Nov 2025 07:36:49 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f49943e42eb351777cdc798cce61f1da3700f702f0c714024799499424783bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146211044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4f58961c2f2a0c97dd3a6caf409ef453ba2b1afc96a290f688615eca0314cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:22:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:22:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 19 Nov 2025 01:22:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 19 Nov 2025 01:22:35 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:23:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 19 Nov 2025 01:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 19 Nov 2025 01:23:10 GMT
ENV LEIN_ROOT=1
# Wed, 19 Nov 2025 01:23:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 19 Nov 2025 01:23:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:23:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:23:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c90f858597bca8ce932b97513ae303456c89b93821353bfc96936e47fded7b`  
		Last Modified: Wed, 19 Nov 2025 01:24:15 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a556459878ecb6e2dc086ddb4a5b5df9f572bde036d678bb00972e3895ebd9`  
		Last Modified: Wed, 19 Nov 2025 01:24:09 GMT  
		Size: 16.5 MB (16485265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387463be0ded98e58961a810b39cbccce9729e5535f7d89724569fa014f26db5`  
		Last Modified: Wed, 19 Nov 2025 01:24:06 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65830f0a47f26c388d0283b98ef2bbab7f9b04a30eb6f24200b0c46cee1e267`  
		Last Modified: Wed, 19 Nov 2025 01:24:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d650c816b1c1fc23bb6c68787294e5066f3fb8cb18c2eac2e0c86c9523ac45d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5798dc669337949aa63aa41c1b4159fcd26063e5b0434f016072debb8f53375`

```dockerfile
```

-	Layers:
	-	`sha256:258ab2eecb41ff21c77da8871fe2c7b3d6b554e49ff6ce43d95092b8e41c71f2`  
		Last Modified: Wed, 19 Nov 2025 04:34:32 GMT  
		Size: 2.3 MB (2317044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c69ec9f9a00f84ecfbec12e2c84188771ad771179bd1e22462dd4701fc030fb`  
		Last Modified: Wed, 19 Nov 2025 04:34:32 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:dbc4939aa5f735a3950139e47aecc67a550f59a02009f79a25413a4da7b7d793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139942090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3ee89264c0386f5aabe5034d5e5134aedbd20cbe88d05acfe9fcc73d3c71ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:54:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:54:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:54:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 18:54:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 18:54:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:55:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 18:55:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 18:55:34 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 18:55:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 18:55:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:55:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:55:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e6d736f22fbd16f11de06f0cbb3ad19602da41d0ae18c2694b069ccfe7a409`  
		Last Modified: Thu, 20 Nov 2025 18:59:39 GMT  
		Size: 90.8 MB (90752878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5d8342f93c44d6dacf126ea9a14d62309805585c68c97e6bbb9da98b4b545c`  
		Last Modified: Thu, 20 Nov 2025 18:59:28 GMT  
		Size: 16.4 MB (16397865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aad0ddb852eb340452fdf608ba2b5bdc61310b851df7f82ab6f47f6190e282d`  
		Last Modified: Thu, 20 Nov 2025 18:59:27 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e6e8717ba9ea9a143cd6829c2f884adf6b48d685fd62aad22e626e4e4133d7`  
		Last Modified: Thu, 20 Nov 2025 18:59:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23c80afa96f9a13d4720389a52c34d1cad0cb18c2efd6dce1d7fc6e42a5b89c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80433fecf0c435488d392dd53ae264dd28b14191071d9b677b5e44725fe357c5`

```dockerfile
```

-	Layers:
	-	`sha256:2c5d25bab3fe2f257104faddcdacda81ed7a37228301dca7c5b90c0661ce8816`  
		Last Modified: Thu, 20 Nov 2025 19:34:40 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ddf9d1564be3dfe6eeb1b21963ed9e7f3968460ec17e5e5e33a9f3012f9916`  
		Last Modified: Thu, 20 Nov 2025 19:34:41 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c685aad5fddb0a04735682cc64ba1179213169a9ae9533a15243e8be99f0fb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139046216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdad0f491a2a9f0b13f495a9b1cb201fc33face2379738adbbce5da05d4d28b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:32:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:32:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:32:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:32:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:32:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:32:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:32:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:32:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:32:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e5b57d009ffc8e92434207bf8eddd2800f9112ab5f49d95410a4fdd9ca7de`  
		Last Modified: Tue, 18 Nov 2025 05:33:02 GMT  
		Size: 88.2 MB (88210704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059868bfe57be2b42674c0650828d193b9328e64392ed82608f1aca6cf0f9a0f`  
		Last Modified: Tue, 18 Nov 2025 05:32:55 GMT  
		Size: 16.5 MB (16482965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8601e52056cea1dc2ba97e9c80e1aff620e6931d1e4b37430d8beb3bd250fa`  
		Last Modified: Tue, 18 Nov 2025 05:32:54 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c694032b86b2e60bd020b213a48e04e66e589f05ff2358b29d5b49b7ca544a`  
		Last Modified: Tue, 18 Nov 2025 05:32:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64a04390d73efb3f69d6606e9564cb1603643155f194cfb9514ab37c3a71f523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2ebd9f1f747d3c97ca1c2d7f5443632d7d74d8758a462777621a7fab9f0d77`

```dockerfile
```

-	Layers:
	-	`sha256:78cf1c842dd6b7034e8ff10f4afa2fc6c6d691b147959d81045c4b547e1e577d`  
		Last Modified: Tue, 18 Nov 2025 07:36:58 GMT  
		Size: 2.3 MB (2313729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8292d68d25f19e1f80cd0ad902642afea6500f8dbd013ac5770f3f20ed99688c`  
		Last Modified: Tue, 18 Nov 2025 07:36:58 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
