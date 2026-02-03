## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:9ebfa3133e47ea087bd6ecb091592a698d5c4a8fb623fc068c509addaaf97d44
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:06be86b01637f55eb3f389da3a74c82aa3855158e894c35390bfa0dd81a0456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230217274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fdd1d9b30116d88eda3f4954c670eb7ff1c661c12bd8affd376f4f9cbd1fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:21:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:52 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d500251f85815d5b1bfb3b60db782a080ce74d4a6a6b09bf7412bd3d4d0d5d`  
		Last Modified: Tue, 03 Feb 2026 03:22:25 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2256d8e1207034d4f8f5c5bc8a9704f7c1ebb40c3b9131d71e6e71c78085ef44`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 18.6 MB (18580088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcf8ed43ec53607207ccc3f7a3d308a490387f5d82f6c8617eb262cad886aa`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e4705948c05fd205324d62d8258fcf5d3e6e2d85a8decd651d6e66707a5cd`  
		Last Modified: Tue, 03 Feb 2026 03:22:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:235291573e466238321d20e3c495b14d10b47be389bf5c8c46cc5a21bf66ee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae30d9afcae9b58ada0719769d927330700acfcb667cdb8736f3ef4c0758a4`

```dockerfile
```

-	Layers:
	-	`sha256:96e9db2ea074cbddd087b7e9d22c08d51fe3a8d8ba5cdcb518948551e77399ef`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 3.8 MB (3817341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35f2eedd77ee8850f5894d0b9dc2369af843d72f4bdd9dd1be6fb846ceeb8f`  
		Last Modified: Tue, 03 Feb 2026 03:22:21 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fa28684b74a5f88c92ec68e2af57fc9d43497f198923fb68da6f5a5c9923446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228819302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a352640a8ac624043e03c68977551d4f78281045e272aac454bed4436598069`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:07 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:23 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee447c22cfcf7aa978d4d42a3bd1ba7f806de37e774986f0d901518075c725f`  
		Last Modified: Tue, 03 Feb 2026 03:24:47 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0e3b5db012c419c3106006531bd95dfa0508faa8c253aaf6f8fe041d33f84`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 18.5 MB (18541467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7f17f3dfde84c2e7eb4fa73b239459581f99ddb5d7dcfa7cec5d267d5c7b5e`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6741e6261655c02846bbdc7e66f56ce0a405b55035749a0cc29a013a3be3ce57`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fc18c40b14f3cba549fc492a4d71cb08c432329188664389f7709c80b5e540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c6b13ff32fee7226cc767e77714e19e46360a14f07708e33accf46c88e8a19`

```dockerfile
```

-	Layers:
	-	`sha256:b6787328f7c7eed89a83c7918a18096354eaa8686ad8149222b638a51eda1027`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 3.8 MB (3818218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee98899d6a54b4bb55af46574074d2e4c9302f7043c503a320f5c43d441e01c`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f48c1878fa1350753daf66b16c5ac2f63ebcdca6ae4c05760950c586842b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234205369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0156be6a093654e5ecd8ed7307f01bbfbc2de7ea3ed1cdbe6794fcfd12cbc2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:32:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:33:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:33:30 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:33:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:33:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dee7bbf1b22cac22a69c8ba0ccfbcf10b976cf32240c0fc68816298c5a35cc`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 18.6 MB (18637262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299a39a28bf48571214a8727db93f37115c77d4272436c15de2f185b7e433bd`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd708500d913a6d79da823da8dc786b75272de8baefefd7a3f6b6e92c6473da1`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e2cfa885caf6977b8eb1fad805158b287c0bffea27f857366062fc261bc3158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ec46e36ce3f4e7aa9f05af3775c0cc29e4abc178a94df446d3d99db8963811`

```dockerfile
```

-	Layers:
	-	`sha256:3c2d576987e55b9455584131c55bd90abc70b41e621f726aee1dafb888e933d1`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 3.8 MB (3818341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c87424310c5a3881863fc4f224c0988b707213d8ceae8a9e619b345164c45e`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:99964b7749d7dbbca0d15565868f9d334559318b6a53e96b0b47b3ee1a74b09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228015059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9beae1942623aeca46dd3e6bb418b1e4aaa42a435303fab5d592394c41533d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:51:04 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:51:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:51:04 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:52:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:52:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:52:35 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:52:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:52:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:52:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:52:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed654d72f1583479eae71ff4bca91d394293fa06b9e1bd650a8ac986e87dd2`  
		Last Modified: Thu, 22 Jan 2026 03:57:33 GMT  
		Size: 157.2 MB (157194267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3b20788c6387c4fbe2dc499d444a11c79426dd034d2b09d3c0a9f4d42a98fc`  
		Last Modified: Thu, 22 Jan 2026 03:57:12 GMT  
		Size: 18.5 MB (18531724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1d2519e15646a74971b005163604ab1122a1be762f3a8f0183f198581f660f`  
		Last Modified: Thu, 22 Jan 2026 03:57:08 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dad8c6d71d865c6a9a56b4379c2215f349e53a9914011f504091868bd1c95`  
		Last Modified: Thu, 22 Jan 2026 03:57:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:465a02125cf609092bfd3e8e0c464c8cc6d997b87d6fa8e7e2e136fc343164c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce6ca5f4ab6031224ef121a557aeb493dd2cefbfb2803fc746bd74e2f426868`

```dockerfile
```

-	Layers:
	-	`sha256:dc3fe6695681d77d3fb6034e5a4d175a4690981d943c2b88615521ff10497540`  
		Last Modified: Thu, 22 Jan 2026 03:57:08 GMT  
		Size: 3.8 MB (3807818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a116071f1710973782c5f679cc085f46d78b0cca93c70c9d80f998cd6d5796d2`  
		Last Modified: Thu, 22 Jan 2026 03:57:06 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:02e7718559ca71f64c3148505c158fb73856dc86189831eaa1ec0c5fdda4b704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219563494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07d7dbf523df9f8d06a4660c8259dcb7458bb98a244d32121aabf6bf7c1d442`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:04:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:04:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:04:12 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:04:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:04:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110ef213ad849aef62022029533be2a09b2a6759b6635f693b2cbce0bee3834`  
		Last Modified: Tue, 03 Feb 2026 05:04:42 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603af855b1a3c5556978a6c32b7d5d8643f8dd7f6dac9760474a4768b12e30aa`  
		Last Modified: Tue, 03 Feb 2026 05:04:40 GMT  
		Size: 18.6 MB (18621114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb2a937986bdfe1e4ebee545e2b201130f5386f82b039f6d8a4ffd1c2aa816`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84836de895b1d4d14ffc23d8f396436f8b0c1303fb848786309943ccb2c6fea2`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d1680189029dd54d28b8b09a6d8f72be723591be5ff86a989bf0316ca54b7e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f776da87d0d253f46c63a26d137ca146e6856943354cb5713274b527c6ead9b`

```dockerfile
```

-	Layers:
	-	`sha256:335323df7b8ebd3dd5740d436800fe6ee77a802398f8ed646a030a8d29f471a2`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 3.8 MB (3813768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587c4a60de4354ea9b26569629486e8291ed07633c6aacc412e61c33a214c1cc`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
