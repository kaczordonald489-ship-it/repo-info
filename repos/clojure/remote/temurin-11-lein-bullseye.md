## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:4ad19a43b088062ee72f675650d14a37cdde109a2bbe6ff92ad8853a0a0adb3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ad61d81f8a0555016c3eb9cb6ad835892e881b80ba8f31c8dc0cebb387253b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219848420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3815ffeb07d6c931a28fd1c915b51d0b94ae3cc7576db70cdefa5a0504b6728b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:07:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:07:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:07:13 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:27 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825af142d4922b4c2e2f373c632a66bee33fc8365d05e1b8723ffc048d56202c`  
		Last Modified: Tue, 18 Nov 2025 22:46:31 GMT  
		Size: 145.0 MB (144966633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9190901dc7e050daf0000e68713196a2a80a486603c6580767e4af190be398`  
		Last Modified: Tue, 18 Nov 2025 06:07:57 GMT  
		Size: 16.6 MB (16607575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7098790971b1507350ddc3a66535c9ab029148774852b975e6889aaa31b647f0`  
		Last Modified: Tue, 18 Nov 2025 06:07:55 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:435febae342a4297b62aed3156442be3bcb5d106d8032011220ade4dbdd25bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd76a33439467d1baa79f2c543ea3f79506553f625380eeb5c4aa69db10274a8`

```dockerfile
```

-	Layers:
	-	`sha256:fb77621f51fa5d9a4a9bc2ef3da76989711d0ca14203e94fe32f51d0cae3b2ad`  
		Last Modified: Tue, 18 Nov 2025 07:38:18 GMT  
		Size: 4.5 MB (4496329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192cb3552d401663d2a8622bb372cdba413e97072bcc05130a8ddd81c92e9231`  
		Last Modified: Tue, 18 Nov 2025 07:38:19 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8476a6c39b358d7c62355cff5a52162ced5e1ad2c0fd8128a5f2b19cf62a253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215102077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e0ce6be5c992f59cf47b28416cb38232f0ced40b81a1ab8cc6f1c5af1371b0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:56:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:56:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:56:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:56:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:56:31 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:56:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:56:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:56:44 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:56:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:56:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2267716489c2a4df43e715db7e6fae8fc49fc583e7387e4e123087b02d3e2016`  
		Last Modified: Thu, 20 Nov 2025 21:35:41 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a00f74c72e4acc9c928be65c82e2e581624ecdb6a6f1df9a0b5f76c4a32dbd`  
		Last Modified: Tue, 18 Nov 2025 04:57:12 GMT  
		Size: 16.6 MB (16595020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caab8d5de706f922f2cef46cbadc138e72fa886cfcd3cf219484678dedf6955`  
		Last Modified: Tue, 18 Nov 2025 04:57:11 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:329c29609225a48a369bd05adf1b7249c24c3109899ffd8cdf36077db5da223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb906819d3248d3974d83e3a7e8ab37c7dc584caf0ff7111e1ea3390eddfc58`

```dockerfile
```

-	Layers:
	-	`sha256:9f8138d3e01bf00a1c750d291faded1f639f7c23e8fde4c8796578a4cdf9d29d`  
		Last Modified: Tue, 18 Nov 2025 07:38:23 GMT  
		Size: 4.5 MB (4495921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e8df9b11dcc6f83039db4d14ce8fd7ae36465fa825669deab72ec5d7d237f58`  
		Last Modified: Tue, 18 Nov 2025 07:38:24 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
