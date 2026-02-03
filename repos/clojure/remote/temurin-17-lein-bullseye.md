## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:90706ebc345b902fd7c6d16179a1211d101c57df3f7be50762488476174f1000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:02c6df5168d474ea6a918f8c2afc6fca0e2061fd55cd456d115a62cd5a78b4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219730007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7481f5687023aa8019ec80d4d43d9d7b2a684fa6749b1515bf1a1ca90505a9ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:09 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:23 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6df87ed0c73fd9755cf9409ced782b70910a3cdb25ce2b13ebd29066944b852`  
		Last Modified: Tue, 03 Feb 2026 03:20:43 GMT  
		Size: 144.8 MB (144847978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bf80af790a500292d1a8f2e8da6f5b474c5925461a25838cbcac6fb8e9d94e`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 16.6 MB (16607616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80288270f7744d76661b71994f3c435c277760d8283ebfcaadf745c2d252e3ab`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dfdc31b924a54767abefe4a40c15c4c8ad60603c252c8ba9252b6bc289e974`  
		Last Modified: Tue, 03 Feb 2026 03:20:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ffb4a052d98c543a569c594269dfb15f4c9c61c6f72693f390538cd9e96b884e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87e1a431aea068990192973c9bd1d0ae9cf20a7ff8d7757f29e0066cb9148a0`

```dockerfile
```

-	Layers:
	-	`sha256:b1a8aae037018ec964fff1377fc0598f6b4342fbed7fe60d08d64d9a968578dc`  
		Last Modified: Tue, 03 Feb 2026 03:20:40 GMT  
		Size: 4.5 MB (4476190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc189cd881979a1ff38d1d03d17f082154f20b21b50903cf4652dbfed800b21`  
		Last Modified: Tue, 03 Feb 2026 03:20:39 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d16ecd62525d0f12e2a2524ad2db9e189c7541b574339e1307ec65ef6d198f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217051480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3abb005061689c741360c93b0e83dcb9b279b73bb9965da7aab9a168c1f830`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:05 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da478ec89f901331d03c8946f08af56632ec018747cdd9434926d9c6e37790a4`  
		Last Modified: Tue, 03 Feb 2026 03:23:27 GMT  
		Size: 143.7 MB (143679932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4c5ebcff673755b691777730cf8bafc119c91b32bf177387a821c6e0d35963`  
		Last Modified: Tue, 03 Feb 2026 03:23:24 GMT  
		Size: 16.6 MB (16595047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b26a996ff997f1ddc631c72db9689b943f94c90a07da7e27c748167be8ae5a0`  
		Last Modified: Tue, 03 Feb 2026 03:23:24 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea12681a4e2134a8235b7ffe370f5c009abdc56cc08fd902569e4b5445b78cda`  
		Last Modified: Tue, 03 Feb 2026 03:23:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f32aa8b04ea81179e8e3b4d531a88cb4da66ea4a352e978e7cdf05043871a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a6186d431660dd215cc441021d87489e6d835ff1bf2370925bcb0f331f2b1c`

```dockerfile
```

-	Layers:
	-	`sha256:eb456a0c4b72d5175190492104ec4e77cd9c9b0fc5e995b98707a2904b5bfa9a`  
		Last Modified: Tue, 03 Feb 2026 03:23:24 GMT  
		Size: 4.5 MB (4475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aee8256b92922178573067a17745290d67c3860f6934d2a63d9ede3544ad192`  
		Last Modified: Tue, 03 Feb 2026 03:23:23 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
