## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:b4f0f6e62c1ae332540faf124ad45e5a3d1c30c5a5de9a1250fb327cb77ead25
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:707bf7626839916915edd0a89e382cf660dfad5fc1c8afe940288fa816246cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217239180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2814602ac233f59b4ba1870b8efa75c359d193e1d5a0933f0dc999cc1158fbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:21 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:39 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf6d6cb3555cf374b8a09a171ce43706e83f88bfa269672bee4b898004ac22`  
		Last Modified: Tue, 03 Feb 2026 03:20:54 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396b5b81ace1a3c4f0643ae3a6eb0f3d35451b5999fd1848e41f61a26df76a7`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 18.6 MB (18580140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88577f5605bbb9e109ae290f966f1952a81221c0546484607ad481a74feaaa`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a468deb34991af8de42777235ed632e9931d10b2ee14200287a9d36698cf05`  
		Last Modified: Tue, 03 Feb 2026 03:20:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3ece8c586ca5bd617b347003e53ef0a5b6ca7c61d9a18ab7f29ab51d20bef649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7fb1804ec970b16a7638b97f8a22c086b1b6d1f70192d5ffed6b4875c4c52`

```dockerfile
```

-	Layers:
	-	`sha256:d7359c0dfcedbe918f4dcfec0e39e86265de0c07acff6adba2f6010fb2b33e1d`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 3.8 MB (3814239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9111324f88e42c2913240039f43300aeca5288d258c847f598eba651e0d1523`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44ea478b2f4a0374402d01b6830508328837738bbaeb2aab4d3a3796347b411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216391599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9043e16efea340ab94e689a2e7c65c9d7379be6e1750cd9a06a122b5d1c0fce3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:17 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e7eb8766a332e5fd2f1c0233c2799b48bd6207af24e668730b484bc6b152e`  
		Last Modified: Tue, 03 Feb 2026 03:23:39 GMT  
		Size: 143.7 MB (143679932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a1fbda2eb08bf92d1317069111195b8a6eae3939634c239f6f8d35d990db9`  
		Last Modified: Tue, 03 Feb 2026 03:23:37 GMT  
		Size: 18.5 MB (18541509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964349f8322f0027a1e93657b84bbad3cdc59e029cd163a7d69efd75f4b9b4c5`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1e00d1b483832b27ab970af6edc0e81bdb309c0e5a3392e4f3198f526b0e2`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88b53bf44deda0ff97e37e0c4a48e3b788bcbeab24dd505afe3357dd6ac2878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879345bec8048d90128056a1a98093b983f04b4f5a3120fe84679f6eaca25a6`

```dockerfile
```

-	Layers:
	-	`sha256:fe0366d284c749f29373196a3100d5f1eed309f3fe0516762da3fffa21e2b507`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 3.8 MB (3815116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:badfa43f0f87b86648cd8d44566a149c98cd885e3d584c84085ab67f3d3c951f`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e43fd6c54a637ac58ff600273f307f2ed4087ff913925f7e8ffc4bf9d745d81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220787159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750d5101f0efd94c685c822bfe4d7a2096c6f7c214b905734f7edbbad1c816b3`
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
# Fri, 16 Jan 2026 03:17:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:17:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:17:29 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:17:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:17:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:17:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:17:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf15ee3631779c5e8a10fa679c64130a5b54ad0969e061ffe1b160beac0d5`  
		Last Modified: Fri, 16 Jan 2026 03:18:34 GMT  
		Size: 144.5 MB (144524715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a62236b2638faa68d0b09541095c7181e2e374730d1e86f8437787fe943dae`  
		Last Modified: Fri, 16 Jan 2026 03:18:39 GMT  
		Size: 18.6 MB (18637296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c09c3f0f5238a782df1b6b3b918720a39f5edc42b03b2e1fb92db3b4cecb60`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15084bfb054805a9bbbd4ac313e5a8e9f108c81d760723d541f73def9b8ae534`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f65fc9cf6db96ece203b16d939e4194d783e9a1ebd31d297137eeb3d86842ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2419584bd539e548368ad66a8343e3aa2ba07382a7b937137715b6a053497619`

```dockerfile
```

-	Layers:
	-	`sha256:dde42d0fd992a9ea5fbecba326be9cb4976168e9ce7e213885b2053288256cc0`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 3.8 MB (3815239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb3852fe56df27bf2aaada7ddaf19021ccab492fc87ca4f38f62eb217ee50c0`  
		Last Modified: Fri, 16 Jan 2026 03:18:38 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:72cbf67bae251faee1c9f121f51ca8df093a61fec9abf5ba8a57170dc6be3617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212710365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0220ad6b7898aaf5ba676aa3e8bc26633a0060c004ede976896d33eff1313c44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:13:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:13:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:13:16 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 03:13:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 03:13:17 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 03:14:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 03:14:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 03:14:48 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 03:15:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 03:15:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 03:15:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 03:15:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f2dc6ee466bc891aa5bacbe66750c17f24c66ed70eb75e898c457e89e0b77a`  
		Last Modified: Thu, 22 Jan 2026 03:19:08 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fccd29ea1f73e6ede424ecf91bb3ae4554cbe65b75d56b38311e6510bfd2bb`  
		Last Modified: Thu, 22 Jan 2026 03:18:49 GMT  
		Size: 18.5 MB (18531741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3031736ba6eacecb2a4e5113011503ac3304187aa0f151935aece4f5c3a12`  
		Last Modified: Thu, 22 Jan 2026 03:18:46 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6630b0606e0c8c49a5c8aaa952282c8887f26e514e26440f324f1aacd0b56a`  
		Last Modified: Thu, 22 Jan 2026 03:18:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:17035536c89e4d7c5bd5f9419c9bfce05d106f1a8e83949f62483e6afbe2e892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715d5750ab32d404da207ac99188407ffbb5d1713b98dc7cdec1196c73fde232`

```dockerfile
```

-	Layers:
	-	`sha256:931aa201b913e7e414bc52ee52bd454380a80cd72ce8d909e54bb5dfe1cdd9db`  
		Last Modified: Thu, 22 Jan 2026 03:18:45 GMT  
		Size: 3.8 MB (3802797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6868c2f4cc7a73de460a19a247a55f019553e395d15829d27b09739833ddab2e`  
		Last Modified: Thu, 22 Jan 2026 03:18:43 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:163ce8d369c57a91846c64ffb8f4b26aee369ec6becec44d2124d769174ed7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207353364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c39c11c647a48da919172ed8a992431caa61d022149c1a6be3ba7df3bf10471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:02:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:02:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:02:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:02:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:02:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:02:12 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:02:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:02:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:02:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:02:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0521af9429b24592bd981b694df00f2d02ab05a0bbb63192b66fd3a113c887f`  
		Last Modified: Tue, 03 Feb 2026 05:02:39 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb775aaffc3678941b32619acc50369476f95f6b1b2b3e689e5e2e10b968e2e`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 18.6 MB (18621037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9297b5a18be3013f48e22bcf11cbe69aa90b881191f748353be6170f772f10f`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccdca359c7a5225df526c919d49bfdf6f043f91ec126af28b6eba43fd12d286`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d6e646d5fa499f93f2c8abd80554f11443fb22baaaa97e4917cba03187826deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f1ef5caa90d7c97df85a182b8772fdcde771909ac8e9fc72793356e32fe19d`

```dockerfile
```

-	Layers:
	-	`sha256:96458bafce479238e9867b3f0af22d5e150a037ec12b7f8f3cc7dbc4841c857f`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 3.8 MB (3810666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ebe1b07d83a7a1c732e4343edc333adfabf834aca1e4a9ef2515df98ce4087a`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
