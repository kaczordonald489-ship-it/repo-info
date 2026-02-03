## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:dde43f20e6e6350e6ef83b2c47dcdffd5a0ced8361ef6e5af31eb90c1b687d61
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b8a61fd849c7d6d76818895cf4acc270515ad6223ea9d9cfea8897029a85afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195591931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04336cbd9b0cee7e453f96113609925415c8866150433b5a08bf1ee33c6fa8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:37 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:53 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab2e03fe6e694c7e391b5c516cd80322cdb9af1c6d311a7e2b9375bc2ffa4c1`  
		Last Modified: Tue, 03 Feb 2026 03:21:15 GMT  
		Size: 144.8 MB (144847977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1f0ec7734c695b38934ae71cece0726f4b90b24219b90b0e19209612332952`  
		Last Modified: Tue, 03 Feb 2026 03:21:12 GMT  
		Size: 16.4 MB (16447168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ef9bc867fcd7bd1e24ebc8e12e6a872ab5996042ae2b7833eeb5e622bb7366`  
		Last Modified: Tue, 03 Feb 2026 03:21:12 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2be4e10dcb64e75e3bcee6fcbd8b1c650b4a9481a69b5b60deb9c6c75950ca`  
		Last Modified: Tue, 03 Feb 2026 03:21:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6db33fcc07c38f6aa992a94f081f04c6aa61c47475f063cba6555dbbc03bd3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14990adda4ce0fea83e9b542dde24e4a09dd9ea05a88f682390d7fb8a42a04a`

```dockerfile
```

-	Layers:
	-	`sha256:8b523dcdda68f68aaf36abe731568d680f1b0ec662e022d247cdb5a1f9278e8a`  
		Last Modified: Tue, 03 Feb 2026 03:21:12 GMT  
		Size: 2.4 MB (2363500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f2031a121a0308793412beb10cf162f6b7573f44a5a21e748734cafccf81c7`  
		Last Modified: Tue, 03 Feb 2026 03:21:12 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3bb282efc611338ac482b5ac4fde9cadfaceea13dcb4869ced20bd12458ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194751779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af31ac12b80311d44c564e328023d9bd36aa3a48be7bcf82fc882b1eed47c435`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:08 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:26 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f06ec4fd7a1aa89b6d95b37c3fc43ff309f738be13b5520bcd1e1b0717ce03`  
		Last Modified: Tue, 03 Feb 2026 03:23:48 GMT  
		Size: 143.7 MB (143679932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58199a45b15059db0d0232c362caf1c5908f07c3136ea4014139e4f0a1edfdd5`  
		Last Modified: Tue, 03 Feb 2026 03:23:45 GMT  
		Size: 16.4 MB (16413593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ee44e91140dd070f830eae2874cee43b8c0cd4ec70a8c5b252a662fcca261a`  
		Last Modified: Tue, 03 Feb 2026 03:23:45 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edcee82eaf3909ae2aa8b928e7cb3426407a05006a6e8f029165700bcfea283`  
		Last Modified: Tue, 03 Feb 2026 03:23:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e58d0bbbe8172259c53fdc6b0e48c2cc3a13381ba8a34fba408b959b0741d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e209a3c28e3ffb155c2d8b21371854e47c1b2e019403067495622ec22f4a13`

```dockerfile
```

-	Layers:
	-	`sha256:1af3bf7b73cc2f407e6fbe9f7c8d0016139e10feb928cc3e39ddfce7ee829c45`  
		Last Modified: Tue, 03 Feb 2026 03:23:44 GMT  
		Size: 2.4 MB (2363118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233152565b399d1450e33fa3cce36ca130445ab435e653f0ba835b845c4b180d`  
		Last Modified: Tue, 03 Feb 2026 03:23:44 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dc67015feb4838cd79d12df2782924171c5453d9ca0684e1320fa33aef9eb77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199123966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2099826852357cddfa667db1a8452707dcc36e2ee3104b60dd5e0aade802e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:16:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:16:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:16:28 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:17:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:17:28 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:17:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:17:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:17:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:17:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf15ee3631779c5e8a10fa679c64130a5b54ad0969e061ffe1b160beac0d5`  
		Last Modified: Fri, 16 Jan 2026 03:18:34 GMT  
		Size: 144.5 MB (144524715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e1bbbd6be4f57f2a0e336422324275798bf287c6a9f8f5a2f5750662a0dbdb`  
		Last Modified: Fri, 16 Jan 2026 03:18:28 GMT  
		Size: 16.5 MB (16485497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef96dab9db9f2381373f18a2fe1acc21817dff830adbbb87147bae7bf5ea7b4`  
		Last Modified: Fri, 16 Jan 2026 03:18:27 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a63ec2cbc40493d47e795bc50899558121a3a9b687104581381938c775b297`  
		Last Modified: Fri, 16 Jan 2026 03:18:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8107203dd796a4ebea6c1d43d3af7ae78ffcb9c3bc132d673b27261530530fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399df3cf2c64626dd80941335778fe9147f0c8b96608cc40b36abc79507005fe`

```dockerfile
```

-	Layers:
	-	`sha256:995e54183dab9c4210eed5a06a747ad3d53ac37b46e34a709ec59bd4643e5d65`  
		Last Modified: Fri, 16 Jan 2026 03:18:27 GMT  
		Size: 2.4 MB (2364480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6fe7163b1ce6ce9c8d10558859b62069a1f748f09f168a18dbbe7d40bc732ad`  
		Last Modified: Fri, 16 Jan 2026 03:18:26 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:0effc731dc4c7c39059835f82b82164b72c8922a1e7ce3dee4f8e6f4197f7bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191077375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d10642acc3235bbe61691d8c583c636cbf88a75d71a5c3b79039c17406e81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:19:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:19:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:19:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:19:39 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:21:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:21:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:21:09 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:21:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:21:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:21:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:21:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d6703bd7ec61f713e938855e33bbe26ef7b2a1842e48351e98a68529195288`  
		Last Modified: Thu, 22 Jan 2026 03:25:28 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f6e22701424251b5c426402ab502ec93daccae39acb64ecd3f5e37ce15f069`  
		Last Modified: Thu, 22 Jan 2026 03:25:10 GMT  
		Size: 16.4 MB (16397905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a51d2904e0b3f96de87b0b29577142f2d57be0c8343475b5eb9565019b992f`  
		Last Modified: Thu, 22 Jan 2026 03:25:07 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036280ed2253f4c3d0868b0c877ecebbc3af60aa12fc7830f86c35336efedafb`  
		Last Modified: Thu, 22 Jan 2026 03:25:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65220ae4e15f65e685b00cd46caceafb70bdae4a6ee3bf9e8e5ce14cf022651f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245b2a48eb0e70fddb687b2f22b58a528a26f304f2a66627ddf464a43c1b4582`

```dockerfile
```

-	Layers:
	-	`sha256:852063297acbdff76b6a273fd94a72fdbd3842429736a76af4997ba98a1b0eb5`  
		Last Modified: Thu, 22 Jan 2026 03:25:06 GMT  
		Size: 2.4 MB (2353629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbe35e2f3f6f661d984f88c1a3ae9dfc0d135eb8a1f5e3ef4d785b198777437`  
		Last Modified: Thu, 22 Jan 2026 03:25:05 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7aea74585ea119231789ea03ac1931e99e8b44e71106c22ece58e40b40e0dbb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185699478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8882173c5001673b3a8462faa3892aac0106c8647aaf962cd54ff808680abddb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:02:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:02:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:02:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:03:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:03:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:03:01 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:03:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:03:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:03:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:03:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6757fa1c248d50fc3a7243e75610057a293d6d883731114d2323093252fa19ac`  
		Last Modified: Tue, 03 Feb 2026 05:03:29 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187c0cf4ee96d492f0c04a399d43f11e9ac8104047c52f880ea1ed0d0acbbb9d`  
		Last Modified: Tue, 03 Feb 2026 05:03:26 GMT  
		Size: 16.5 MB (16483425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca3afad0dd4c549629d323d936bab7b834e7c4e4845ad19d120a7ee38dc0bb`  
		Last Modified: Tue, 03 Feb 2026 05:03:26 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fc4c4e5ef2625efacb1776fbc785b0e82153e631af512f60996cd0a0f316d`  
		Last Modified: Tue, 03 Feb 2026 05:03:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cd7481df4cacd780edc9cdfc541f19251405dff20048e00581b085c01517d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c4f9493270dbdfc0ee55342ec34a0b5f7fdd937a7ec39ce734137c95711ce`

```dockerfile
```

-	Layers:
	-	`sha256:9933c24920f94981537f55767a4f15766bfcdd7560440938c8e053e9adb1f669`  
		Last Modified: Tue, 03 Feb 2026 05:03:26 GMT  
		Size: 2.4 MB (2359927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f41fb77666215527870253d932643d06adea2a00156a0032b4dbe916ecd28b8`  
		Last Modified: Tue, 03 Feb 2026 05:03:25 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
