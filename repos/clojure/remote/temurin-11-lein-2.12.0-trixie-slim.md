## `clojure:temurin-11-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:d13fa162e82b049d210e4441e6c701576978c7c7590875c7aa878594b290dbab
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

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c5697d02e98d96947440c46253b37d1f9ab7f1ed5f857c33c27d38dce8e13dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195707962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f88b228ccc57ad62a103ac4a7367dfd16231aebe5ea107b0643578f505324a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:07:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:07:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:07:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:32 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:33 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43db471761f670a515c691194a2cc5e570e9d3acdd8863d744e6d75915f446a6`  
		Last Modified: Thu, 20 Nov 2025 00:01:44 GMT  
		Size: 145.0 MB (144966608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3192c5fb0d74056e0cd47531c7d0cf4a5e015d942d842580c6c22b545df47c03`  
		Last Modified: Tue, 18 Nov 2025 06:08:00 GMT  
		Size: 16.4 MB (16447117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aa9a5ef8fcf0d3481389bdab2040b59930cc7d977952503f5128a0f46717d0`  
		Last Modified: Tue, 18 Nov 2025 06:07:59 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a04b3e786e3166dd8a29c0090ad4f19ba22e9548b4b15d60961b68132acbae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce27ae6f38b8a4ffd148b26b6188a42092a449e9ce866eddec0eceedf4530c1c`

```dockerfile
```

-	Layers:
	-	`sha256:54ce8e60cc2fdf34bb14bd9a01ccabbc5a4437efdc9d73f8446dc58ab3957e38`  
		Last Modified: Tue, 18 Nov 2025 07:38:51 GMT  
		Size: 2.4 MB (2383577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702b4d5c8667892640f5f97662f4238c089088bbad0ae84e19cdfe391b55c099`  
		Last Modified: Tue, 18 Nov 2025 07:38:51 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:156ddaf34f6f6c380221a58dac51f9a01cf877e4982479844d29d4567c1dd76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192801787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c580e998b4d3d64a291f239d0e649d2311c55a488ef4ee7381ae24433ef915`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:57:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:57:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:57:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:57:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:57:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:57:42 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:57:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:57:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687143b45f2745c66e893ab10cdfd060a836368a657370ffdccf23cea8ade095`  
		Last Modified: Thu, 20 Nov 2025 03:07:18 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946ab1c048531cbb9fe5945724e79e5ce11bc849ac79583a4944180da8980751`  
		Last Modified: Tue, 18 Nov 2025 04:58:10 GMT  
		Size: 16.4 MB (16413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5544c87c2a1f636684782f0cbe71a811b8577a6a200cd20b91076b4fd0905c`  
		Last Modified: Tue, 18 Nov 2025 04:58:09 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c38671dc80220138fcda9b2953643f06ebfb1a441b2409c01c8b28d26902b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e102ccea3ae5cdd63b31d73385a177828215d62a6ee40fdc09dc4c3cb0d8c42`

```dockerfile
```

-	Layers:
	-	`sha256:2933bf0992ab4a74515bd8ad0d2e18ac5861639bc121f757107403a5c4cadced`  
		Last Modified: Tue, 18 Nov 2025 07:38:55 GMT  
		Size: 2.4 MB (2383813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e70f1a78c621799998d19ef14b82024a233b116449ba7bad1ef289b640a2899`  
		Last Modified: Tue, 18 Nov 2025 07:38:56 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e642cf4da3ec513284c4da14caad9adae6aa487641a656aebc67dca3858e1172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186681837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac62ea2d539c1b310c79003e7bfb4932064decd7a5ae2bd55d2da9bc75ca4d4e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:01:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:01:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 19 Nov 2025 01:01:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 19 Nov 2025 01:01:36 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:02:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 19 Nov 2025 01:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 19 Nov 2025 01:02:17 GMT
ENV LEIN_ROOT=1
# Wed, 19 Nov 2025 01:02:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 19 Nov 2025 01:02:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101726268a9c7a9db9d3928c7b9b7b5dfbe85749cb3ffe52f90f89f43094039d`  
		Last Modified: Thu, 20 Nov 2025 00:01:33 GMT  
		Size: 132.1 MB (132081949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31421b72b742d65506769a8b6b836f2e44220f0483f36ba840bf457b727c70fe`  
		Last Modified: Wed, 19 Nov 2025 01:03:10 GMT  
		Size: 16.5 MB (16485244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f17fd4fcc5918abbe38af68a1fd0b8c15c5786c3db6a231cebde956f4050f`  
		Last Modified: Wed, 19 Nov 2025 01:03:09 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec180b8bb8359da4e81b1c05c264b332f87945ba96e34281cff0f9ed0be736ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db324ac7e1b3c85e9f05854c16e9621e324d93b6767175daae8c774646973793`

```dockerfile
```

-	Layers:
	-	`sha256:835e7c092310be66c937d2306436de2ebc79ffaf6966f90b970731d46f41f836`  
		Last Modified: Wed, 19 Nov 2025 01:34:52 GMT  
		Size: 2.4 MB (2383942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4360efed84d7c3219e059531eeaa942a4e835765326805b4a1fc02d122442c26`  
		Last Modified: Wed, 19 Nov 2025 01:34:54 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1b292dc3e7e9b1d6006b0b726700711a597a8ec10cc3c4bfe244066c653c349e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176529538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5faeae99c9fee6ed7b541c5edd28bc949d843cf25ad0a505aa2dce010d645736`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:22:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:22:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:22:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:22:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:22:53 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:23:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:23:05 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:23:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:23:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1190da05ae19a10b46e3d831eebcdbad7fda228e722f28b4f162aae378b135`  
		Last Modified: Tue, 18 Nov 2025 05:23:45 GMT  
		Size: 125.7 MB (125694433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ece5246e10e7621dbff7e7d3eaeed4f75fd6d6d44c2e43d2b97b1ab3e03afe`  
		Last Modified: Tue, 18 Nov 2025 05:23:36 GMT  
		Size: 16.5 MB (16482987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f07013c350d6757635035b4709c0fd6792265cb85266e1b79d992178a260a3`  
		Last Modified: Tue, 18 Nov 2025 05:23:36 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d1bc8b23f76772d0a737ecd81a6d3aafe5fb2d8ddcd803febde8f057dc80027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eb09691ff77a8aabdf8babf9fc883a3a5f11b830f7dbfbaaaa27d988fa2906`

```dockerfile
```

-	Layers:
	-	`sha256:4169717ff7ee7349cf033c13473d3ab2d949f25a79890dd096eb92cc70e9e7cd`  
		Last Modified: Tue, 18 Nov 2025 07:39:03 GMT  
		Size: 2.4 MB (2380008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0104a6999a7f46d93af8daf86e4803e16c8b0fe553cf66cae1893b1d6cf9b93`  
		Last Modified: Tue, 18 Nov 2025 07:39:04 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
