## `clojure:temurin-11-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:0eeda64bd0d346f32dd5fc48d0857a60e507c090cf9f4d1edfc37c8442bfb742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:046644cc7a43ccded3f92a6da8fdc43442d5bd4aac56b7b6414af25ffc972efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219848247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad05fc4181a16d18a64a412a58c201edccecb2a8467dd64b40be3e9665bbe606`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:19:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:19:13 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:19:28 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:19:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:19:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345302503c0fc3ebdb465fe16e6f3e5f31d00f920d9834383bb2a69139545bbb`  
		Last Modified: Tue, 03 Feb 2026 03:19:51 GMT  
		Size: 145.0 MB (144966607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a868de4b54c0b5216db468cc606dbe5729c835dfb55a638a980cd7dc360ba6`  
		Last Modified: Tue, 03 Feb 2026 03:19:48 GMT  
		Size: 16.6 MB (16607611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa251406d81fc88af61a5d46bc7ece868624ddaea130b5b867667fcd792a65cf`  
		Last Modified: Tue, 03 Feb 2026 03:19:48 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:72605b24b70ab094801d610b0ae0f14f8d36a8e5bda1df7573d2781011e65251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390e65a87ae3ffad3f7f81d09309417eae05ee01d7d522145a3bcb8b7c440d12`

```dockerfile
```

-	Layers:
	-	`sha256:a36eb99f859c3ff828b8863e8328704edd27c06b7d5ddc4200cf6e4e884632b6`  
		Last Modified: Tue, 03 Feb 2026 03:19:47 GMT  
		Size: 4.5 MB (4496329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b6a92a02e14356ae843fa02ac7fba5209ea8d968c73cdebc8ddd4bcb5ac9ab`  
		Last Modified: Tue, 03 Feb 2026 03:19:47 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:104e4ccf2536b1e36b1ed702dd32228f95ae48941223dacb7ceb34b5e01af899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215101022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18d74f1e07a2a97490a61b383ee75028a915f8e7296868b6d44febc237eec8e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:43 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:57 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a1def3147761fddf05a39c7a50a65cf76465307a6a4e10540e678260dd7c51`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 141.7 MB (141729907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf4ed43f48d3c3cb63e97e825617408b3ab66f0a490cfbe2d45ee77aea1a39`  
		Last Modified: Tue, 03 Feb 2026 03:22:16 GMT  
		Size: 16.6 MB (16595058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46643a60cea453d35765a2e373bf80541fe7134d877493baec907fd9fab34a2`  
		Last Modified: Tue, 03 Feb 2026 03:22:16 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aaae9f353ce9dbd2fe7445419fd1878e3ef87e231698f568b21f999250864a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d93622010cefde6ddd93bd86c713d37fd9338bc705eaba31537f7e3f35f911`

```dockerfile
```

-	Layers:
	-	`sha256:4dd226346da9ce1d3be3b993c308c6f56121f5ee9d1e5ad83110437cc16c8f2e`  
		Last Modified: Tue, 03 Feb 2026 03:22:16 GMT  
		Size: 4.5 MB (4495921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83674e730593f83a5df3836f372e28262f5df32253cc53c947ac9c9dcfff3407`  
		Last Modified: Tue, 03 Feb 2026 03:22:15 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
