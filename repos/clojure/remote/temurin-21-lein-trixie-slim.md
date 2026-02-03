## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:79b237fb24dfd560882aaf3a05da55697f0f3f9e6e0c35a585d4d366d234aaa6
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71b5c7987389498710334e6575e93d1274d7e674507fdd6a0b443541710f65aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208569908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef65ba89f7c17497244023b53b275cdca44a18cbaa9396a0707e6a57b77825`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:47:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:47:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:47:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:47:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 02:47:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:40 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:57 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00f91cba6eb54b531fa1caa636ab9ceb5148dfcacfe78dbeee92b0be85ad11`  
		Last Modified: Tue, 03 Feb 2026 02:48:51 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17077eed7d31aee3d58a3dd0f4c6e155f6a45fd94c57a5bfe2abfd2a4f27b229`  
		Last Modified: Tue, 03 Feb 2026 03:22:08 GMT  
		Size: 16.4 MB (16447171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a7f151f05b630dc04bed393eefbe589df28d84fe51d3698012e7d7444397a0`  
		Last Modified: Tue, 03 Feb 2026 03:22:07 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88f610d9dd58daf53ff9bd4e297873de6f8922c45c5ba0794a57ddf15fae264`  
		Last Modified: Tue, 03 Feb 2026 03:22:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0661323b61266d8848cf1e3be5e2aceab0aadf20dfb4baf13b0a838d029a040b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba3057d84822dd880070677709cbfc9eb9c1008e262073e067b3bbca11e02c3`

```dockerfile
```

-	Layers:
	-	`sha256:85d07a425a499f5c8f213e77fed160621d26e47fc5b50f873cb3d540521def43`  
		Last Modified: Tue, 03 Feb 2026 03:22:07 GMT  
		Size: 2.4 MB (2366602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b06cda1f7befd9b9dbe8445445434b616afcb6d447f95b0c83f06b51878017`  
		Last Modified: Tue, 03 Feb 2026 03:22:07 GMT  
		Size: 17.6 KB (17586 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f2da6e6334ea42e062e29abe087e0cd114cce73bf934a4bbdafb38e7ac9dc2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207179397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53f3944b4c0bf18e3abfee5c27ed48c3cb50b010e3983870cae222d106f2577`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:50:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:50:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:50:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 02:50:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:08 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:26 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d003fbd9f5c12c8a0004482abf6d65cfbd0a5cb00717659781b8c160388bb6`  
		Last Modified: Tue, 03 Feb 2026 02:51:24 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6685347e007a6371d47e195eb0601c817c3349da5c4f804648886e2bf2cd3a`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 16.4 MB (16413553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503290824e9656472c58624f2f43663505dcea0fcaf3e634b8576a3c7fe5c15f`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b02d15050c3e321f6ec55c01b054b76942a8b5aad7c09fbe87902f848dffb1`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60b604b1448c9501b3799aa7d7c8c9d7dc5da8775e46e943d5eac9688365dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0129990119ada74885d42b754feb77dea55766de812e362c00dc2f5ff82097`

```dockerfile
```

-	Layers:
	-	`sha256:0fa9aa797a349c307eab7905ecfeb0b728e95be27fba0040083feb647acf550d`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 2.4 MB (2366220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c1b76ae41c910da10078fb214355006b314480d94470dfdb6c3d132995ec2`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 17.7 KB (17707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1d199da81529806d9719926a1940cdaf4da083d69cfd3091484f1d25ae348624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212542190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2957b090d4b303bd5bcf2ba775e11e6aa40fc3aa021bb10d3660053c7300e088`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:32:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:33:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c4fbbaa8e975bc0429ca07be97ff3f9cf83c1e7ff46128925443cab78ea9f`  
		Last Modified: Fri, 16 Jan 2026 03:34:22 GMT  
		Size: 16.5 MB (16485461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf0edc473116a0e243e43fb61ff4be53eca39e46f27a5f5e5c8b80b2756e01`  
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf07eb97b5e14107a458576a4082f1c80a732fe3f558f05ade81079541744de`  
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1773201d5eecadf1f9c7f2f3e20c8f936de973e4bdf1b7bcedfe0536e1d0d2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab65bcb61f749e3da3f2c7319d265d655ceee0e3d2d68375b7e6f45f1470c4d`

```dockerfile
```

-	Layers:
	-	`sha256:40ad01095aefe1a3792c77b22572ed2bf43aa03540caea79cd60393cf681d209`  
		Last Modified: Fri, 16 Jan 2026 03:34:21 GMT  
		Size: 2.4 MB (2367582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988fc7fe1721aa3b1e0de76d295b6472bb34f25318c6c0e35f8882e3fd5ac8fb`  
		Last Modified: Fri, 16 Jan 2026 03:34:20 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:a06413c72c07d61e0e3329fb3ead91ca3d94d447c645d1f7f1bc6a7e7727618d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206382137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c0d9bd3fe865d6143e0a62ee7f70b6584ae2e00d878de0fb016ab0fb3d2fa9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:58:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:58:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:58:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:58:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:58:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:58:06 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:59:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:59:35 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:59:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:59:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:59:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:59:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce3d8fe97e3f0f300cf6a379bdf8a6818893898d0842fdaef865eeba68c7ff`  
		Last Modified: Thu, 22 Jan 2026 04:04:03 GMT  
		Size: 157.2 MB (157194340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41a28d163708ea7d7dfccc19f791eed8c97abc8960d03006ce79712bd01f523`  
		Last Modified: Thu, 22 Jan 2026 04:03:42 GMT  
		Size: 16.4 MB (16397911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70147e8942b8894dcf3bc8586175a5a92433859a1236bd7eb4b30e1e91d9b0ef`  
		Last Modified: Thu, 22 Jan 2026 04:03:40 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1978bce5081256c41dd60049a163bc0e4e8183f7e084aabfd6f6a3c23fee0ba2`  
		Last Modified: Thu, 22 Jan 2026 04:03:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9130829ee88d8930691db7688e4a3ca560e2b15f8035bcf18dfff4d4e4ef8e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e9abd36848b4c8321c026151ba568bd14b2494b46c7c5a8d13b7cca1cf4d4b`

```dockerfile
```

-	Layers:
	-	`sha256:49415e4b8aa90d745344413d1c7af7dff752cd3ef5ca74a4f4b224e3faef115f`  
		Last Modified: Thu, 22 Jan 2026 04:03:38 GMT  
		Size: 2.4 MB (2358650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa2948a16a1b175e1a80ff9f5f72670c58836762b3da1796363c31be83e9f91`  
		Last Modified: Thu, 22 Jan 2026 04:03:38 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2a3b5a3619cc4cbe8976670b1a2372d39c95830409196c334f3202426cd43299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197909516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eef77fb948984631f626ba5c4b62a9f2153f5581d74069361db217b39ec408e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:04:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:04:50 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:05:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:05:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:05:02 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:05:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:05:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddacf145453dafd4beb96b06bd9815ba82a596f69a0b76695fe62e6eb186ba`  
		Last Modified: Tue, 03 Feb 2026 05:05:30 GMT  
		Size: 147.1 MB (147069811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29cbb602419df27c97cba75ff39301a288346075a0175a964f71e5b6a2eb7bf`  
		Last Modified: Tue, 03 Feb 2026 05:05:28 GMT  
		Size: 16.5 MB (16483364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df45ce63e9ebeba4c60f85bdf9054dcac94ab8b5fa4e00d5e874b1341ab9940`  
		Last Modified: Tue, 03 Feb 2026 05:05:27 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561aca08ee8382c949ed9aea49e7dc9db7dd1d1ad4faef70f9f55344eb194a92`  
		Last Modified: Tue, 03 Feb 2026 05:05:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70df1c78e0ee906fa4e54e67596dc47c6c1dea0009a8b843ea8dadf9e93419b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb8e6e1dcd9f88ceeac7585815516bbd91bd2de2e777f88a2394e9ced42f74`

```dockerfile
```

-	Layers:
	-	`sha256:b6bc841d8b5c3d5fa3ba35f550eaa929b9494993bb5bbe61060ba2f2529c457a`  
		Last Modified: Tue, 03 Feb 2026 05:05:27 GMT  
		Size: 2.4 MB (2363029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b728d7f61048854f16d70ddcf3208f5643c8a497bcf492b8f95d851365d7893`  
		Last Modified: Tue, 03 Feb 2026 05:05:27 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
