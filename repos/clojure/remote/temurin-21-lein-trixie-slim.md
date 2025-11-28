## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:6493eb3c1b2518087d636a394eadf246d19482d9bbdd7053dd67a6081d06c07f
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
$ docker pull clojure@sha256:9beb835c64eb502cdc14144901a5f3016a8a6f9face53cd9fc8b30df7c40c8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208567808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad23ee463e3329c0cb16be8bce7bd8662b420dc542cf2bcccc1bff204e4e98e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:13:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:13:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:13:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:13:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:13:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:13:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:13:16 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:13:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:13:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:13:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:13:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ca9ec522c0105b79e85b0720f9c6da94909674059a9a6fca215edccf61edc1`  
		Last Modified: Tue, 18 Nov 2025 11:38:45 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e0793cbbb2f6c0d5408092f37a738a6b33546c9e6657ec1fb8252134bd983`  
		Last Modified: Tue, 18 Nov 2025 06:13:46 GMT  
		Size: 16.4 MB (16447142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bd41e2e299f703ca4d16474f1d3dc02d0dd468da9d051578c43c0d06240574`  
		Last Modified: Tue, 18 Nov 2025 06:13:45 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a331bb0059f8d4fd1b3ea13b2a711176183d20fa0619c95b07ace9a16b9ef62`  
		Last Modified: Tue, 18 Nov 2025 06:13:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c4481fe416bed06ff7b4394db789def200b33463692d4ba1101b36c1de2bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac93aa16371cf6f9a839971fc90a743e739bd7ba77a29b18eb9fe0ca0f0d38a`

```dockerfile
```

-	Layers:
	-	`sha256:123318cea77d8eaa020295380a4454c0fcff0e1554381ca397eaa0a8a89a3081`  
		Last Modified: Tue, 18 Nov 2025 07:45:27 GMT  
		Size: 2.4 MB (2366540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dcc97d748592284ed0fd9c56e374ace4ef28b56d56187484fb2b27efb689b0`  
		Last Modified: Tue, 18 Nov 2025 07:45:27 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7aed48ee13853b5af6ea56a43f7c5c973d69bc1fca4af670e5ca997d2973536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207178287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647beb15cbba1de51e8e1d750df323d047c6328c7821219c354f49274cedb50f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:08:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:08:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:08:17 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:08:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:08:33 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:08:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:08:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:08:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:08:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e974ce1e70ad2f909acef3786f5059655c8c35da8b6b8f2a46b1cfe818203410`  
		Last Modified: Wed, 19 Nov 2025 22:12:46 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c6d83fd726055ac72ed33ad0c7dc3f59c96b0896af71518164176ab383f46`  
		Last Modified: Tue, 18 Nov 2025 05:09:03 GMT  
		Size: 16.4 MB (16413819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e873136794096c2c4303f96ca045276a4b6f6df60c4ee22e6cd8cb2fd3c1b3c`  
		Last Modified: Tue, 18 Nov 2025 05:09:02 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e58bb2e4f0b4952dad20bf5840ce0f80d6726f08da5966ee3e79673e014d230`  
		Last Modified: Tue, 18 Nov 2025 05:09:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:486e234de97310e8a7c339f5989cd67b16f51cc9d476fdc0881def81f91baf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a40c06242a77d2a5f0bb6c0251e916c382f5df770112b0e1fc1b0b36ff7ffa`

```dockerfile
```

-	Layers:
	-	`sha256:d6a95c8bdae3a1bd117257244d798e440d891bd1f0ee1ca990a2953e4ace8515`  
		Last Modified: Tue, 18 Nov 2025 07:45:31 GMT  
		Size: 2.4 MB (2366158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefe7cbffa893614410b84083115f086e5509247682c9fdd055aee2f311b907d`  
		Last Modified: Tue, 18 Nov 2025 07:45:32 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4893a6de11644055a38862affb2f6b02ad3b8ab1937776f9a390fdf59d554b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212543109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504a896f809d1513c742ca38556c99dcd7a9843256c2a2dfc584e992992b523b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:20:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:20:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:20:17 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 19 Nov 2025 01:20:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 19 Nov 2025 01:20:18 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:21:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 19 Nov 2025 01:21:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 19 Nov 2025 01:21:07 GMT
ENV LEIN_ROOT=1
# Wed, 19 Nov 2025 01:21:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 19 Nov 2025 01:21:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:21:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:21:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd130f2e8b75792a89896873c54ba2093ec400e1aa0bd5b59bd010122b0df27`  
		Last Modified: Wed, 19 Nov 2025 01:21:54 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aff6592532d8028a8a7aca817e59ebe911f6c4c18306270211e5d3d9fc73465`  
		Last Modified: Wed, 19 Nov 2025 01:22:05 GMT  
		Size: 16.5 MB (16485163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24acf269aa6bcbd0ecd9e818f73ade4eff81a8bc5b300efaf4c692b4e9b77f99`  
		Last Modified: Wed, 19 Nov 2025 01:22:01 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714a0759aeac8de1abcd3f5bd7e0eae408f2a0177faf8c0bd70ffeef4de426a`  
		Last Modified: Wed, 19 Nov 2025 01:22:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94578e66061dbcd0ef8194188475158e59bcc8b0f6e5519bfa4f97b58f20156e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae4b9af62e1e8ff6ff13d5111faedee4ae2bc8807f9119d861005a35f91926c`

```dockerfile
```

-	Layers:
	-	`sha256:4fd2bec2edcdcafc135aba9790030312417e37c8f71674146f803fed73601cfc`  
		Last Modified: Wed, 19 Nov 2025 04:36:12 GMT  
		Size: 2.4 MB (2367520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1001540b91e514b31e15bd3192c99fba7b5beb9fc5c1f5e58807c7314532de71`  
		Last Modified: Wed, 19 Nov 2025 04:36:13 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:896f6f2fe624bd55917e6a11f2bb0586df36d5f5d8706d8197ea93b98e6aa147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206383549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2363ec9486cdf23032eadf3e02707145ed720df2b73ba5ebd9a95461d48805d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:27:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:27:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:27:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 18:27:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 18:27:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:28:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 18:28:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 18:28:35 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 18:28:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 18:28:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:28:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:28:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f07972228dcbc55c70b87824ef60b8072c90f8a8787a93b8e4054d62735df`  
		Last Modified: Thu, 20 Nov 2025 18:32:59 GMT  
		Size: 157.2 MB (157194320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d8e837cc89855d17c99b22159f005e8903ac23af850d4b1c1c6fe833a47e0`  
		Last Modified: Thu, 20 Nov 2025 18:33:09 GMT  
		Size: 16.4 MB (16397875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44afa0f681b4791914704d576f7287e4f9881f79ee2b4d7a253bf5c29a97117f`  
		Last Modified: Thu, 20 Nov 2025 18:33:08 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47719f85e6dbd9f2123c0040575d5dae2b838c7234f9e436722ad1df7fb43f7a`  
		Last Modified: Thu, 20 Nov 2025 18:33:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0f7ae7af418e406de9fe99ef975ddb335fe53ba82ca4f96603b1505559aed2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f250977491e97a239f81f8354f4527bd07d93d5b8512156e9714e363456c6d`

```dockerfile
```

-	Layers:
	-	`sha256:3763c1bac6e2163888af09e5a3b63bc0152f2b67de8870c88ebebb1229d3b1d0`  
		Last Modified: Thu, 20 Nov 2025 19:36:55 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f73c4b270794e831adaa870289aab5c2b2892e9241af425fb7799efb327091`  
		Last Modified: Thu, 20 Nov 2025 19:36:56 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:99bb966bf7f48cba48c7a3d069a39cc6e3c6d87bed6248f982628286a9261a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197905385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e0e9a7d70f61d48a370cebce5fb3f033a41f2cce4b10c5da09fe60b464695`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:29:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:29:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:29:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:29:40 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:29:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:29:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:29:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:29:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15456efc8c56111be75fbb32203283de9917eff33d36ac2a49eec5455d7ae626`  
		Last Modified: Tue, 18 Nov 2025 05:30:10 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d08265487bf5c25e52f405bb7d75e830baea4489a37f1071880837237b4240`  
		Last Modified: Tue, 18 Nov 2025 05:30:17 GMT  
		Size: 16.5 MB (16483007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f33c5fd1ef44d7a510c708110eeefa101ae239efd20d89504fcb553f611d03`  
		Last Modified: Tue, 18 Nov 2025 05:30:16 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9dfc3e1370c26b0b4f9447122ab39f16226884714849594914527bedf2b96`  
		Last Modified: Tue, 18 Nov 2025 05:30:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:092417cf96bb517c0e4d7dcd43b6c7277a918ec6bf0b205fa18a98a06cb359f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae533f7dd7e61d28adb1056c013af28fa204ead063b7a66f443c3ab003ba5b22`

```dockerfile
```

-	Layers:
	-	`sha256:d0189d856ca3ad34371a385d23c8729de9ac01fe6942af437edd3f549780c704`  
		Last Modified: Tue, 18 Nov 2025 07:45:41 GMT  
		Size: 2.4 MB (2362967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8988daace6cdc152c8e4dce7a8b827f7baf9df23436d1ad94ac573a3ed36bb`  
		Last Modified: Tue, 18 Nov 2025 07:45:42 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
