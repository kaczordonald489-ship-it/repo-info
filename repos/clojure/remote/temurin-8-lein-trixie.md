## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:c83ea494228c9551a466e94582e7bde243ab7b765ab01e8e1f99355f78127ecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:25d481c6b80f3170d860de6868e9f4a9e37738e03339bf74efcfe4b9cfb690f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127120336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb2d1cd0a64e24d33a0e1fc6c5d1339a9803c5442240ef96a6ac2c9ab45cda2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:05:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:05:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:05:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:05:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:05:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:05:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25699c93dc7bbeb34f328faa846ea6e7aaebd3e2103f6a7415ab228753165c`  
		Last Modified: Tue, 18 Nov 2025 06:06:00 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a685cae764202c821d9d42035743a783387e4bf21b0225157eeda74292af79a`  
		Last Modified: Tue, 18 Nov 2025 06:05:55 GMT  
		Size: 18.6 MB (18579603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6247b43edc1d16f81f30134ce33f8c9aa7b08f76fb207422651db6a65605f337`  
		Last Modified: Tue, 18 Nov 2025 06:05:54 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3915e42a7a3d9607fc42d5c38ee014433807c152b54db0a52e0b0c1d448b0f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa59d20e81f50264e2d667daf0f5e06c63f08dd7e7027102626d8e22f48958`

```dockerfile
```

-	Layers:
	-	`sha256:828acdd0676ae8fb686171c88ae5117697ae946810ee6dce303003a0ad901449`  
		Last Modified: Tue, 18 Nov 2025 07:50:36 GMT  
		Size: 3.9 MB (3934990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2817e88c9fd09255514710d4340dd5cf8dedd80bc19e4fc6a4648f58aef408f3`  
		Last Modified: Tue, 18 Nov 2025 07:50:37 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:619a4d86eb0f5c1de3a4ec5ca6351d0ffe300596d557571dc99257dbe72803e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126523587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ed5705b5b20edc6e236a3ac9d74f07ae75ed265909f28f4711dafef12bae80`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:51:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:51:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:51:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:51:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:51:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:51:37 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:51:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:51:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:51:54 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:51:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:51:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22549aa150dd4c4a72c29952af1cddd9539bc141786346508c2af30b3f069920`  
		Last Modified: Tue, 18 Nov 2025 04:52:22 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5c9583aa6327225b46d97a26ae222acce87158605d7c079dbe8d03a1d1cda6`  
		Last Modified: Tue, 18 Nov 2025 04:52:17 GMT  
		Size: 18.5 MB (18540594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7b864e8d8a30a1a1f2b047d9b457a5afe60f13de8e871b82f06f4d4518347a`  
		Last Modified: Tue, 18 Nov 2025 04:52:16 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1f1e524587d8154b914e1c9d890a52a75e630f49fae4a5d53f289503a1d218b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43d51330d60c39c5ab123d0f16feb1304a69ffe2fc4a38d477a9963c7da5cc`

```dockerfile
```

-	Layers:
	-	`sha256:30dd571badbbbe947c48894dccda3c19a2c8f0931182da396c907bf410ff6517`  
		Last Modified: Tue, 18 Nov 2025 07:50:41 GMT  
		Size: 3.9 MB (3936565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a544e4e3085d6de1df1e8cac68b0517fbc07bdb3cbc6905f3113879980337b3a`  
		Last Modified: Tue, 18 Nov 2025 07:50:41 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:33cded34b8d008abdcd7a419b749bfebd8d92f574c780caf1c6baf2492f354fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128438555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63135369b84687c424ab6d6d04dc2b81a84ddaf04177c024dd8aa7152359c0fe`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:14:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:14:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:14:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:14:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:14:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:15:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:15:08 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:15:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:15:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d016d9e912cb735827e82c51514523b6941a4ca5114f7db6b8ad862763e4a5`  
		Last Modified: Tue, 18 Nov 2025 06:15:45 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aade8195fd59435203fce188d5a77b2ff1d4283767420a8c299c5be1ceb1a0`  
		Last Modified: Tue, 18 Nov 2025 06:15:50 GMT  
		Size: 18.6 MB (18637141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63aa39d78f643e50082795bd5d119aebc497170220c5492ab7fb6081f3f6d37`  
		Last Modified: Tue, 18 Nov 2025 06:15:49 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1bedb313e5f2aeab7c78f51a4aea717ea10bd6ab156a06297133d7f7bb223b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bbeb9509bb41755d114b6cea4dac36dbd3743acf0c730b445e8a2c9020ca08`

```dockerfile
```

-	Layers:
	-	`sha256:bef7094883e20d7beb08aae0ddb8c0550d893105297aca82d19e45dc93d355ba`  
		Last Modified: Tue, 18 Nov 2025 07:50:45 GMT  
		Size: 3.9 MB (3936581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d975b994b470f7f2f498c7e4dce6c2f43173e9f0e72932279d8823a60fb7750`  
		Last Modified: Tue, 18 Nov 2025 07:50:46 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json
