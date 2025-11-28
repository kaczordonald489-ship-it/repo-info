## `clojure:lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:97f7dc2bc2ef9aebb6f42a34bd17813cc25792e7771c8a72ec41e6dc3b144c33
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

### `clojure:lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7f8aeffad75b28a319f1a63212a501a3440c1ef9cb3ec2f036602ecfbeab15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142549996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552faef707387624c60945dcd4deb4be955ad1c666edc57a73941f17600ff61e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:15:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:15:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:15:20 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:15:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:15:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:15:33 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:15:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:15:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:15:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:15:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87a8497aefb6ac33c53b359121a3420a39136e9a68ed42d2473792ca85dae23`  
		Last Modified: Tue, 18 Nov 2025 06:16:04 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adce0a4c53d3499647248d69887dde8107aa39e896a2d298051dc464d61868eb`  
		Last Modified: Tue, 18 Nov 2025 06:15:58 GMT  
		Size: 17.8 MB (17758081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963c88f10a442ec3ef3ff33ae2aa9208c984bbb3dacfe3ebe818fdbbe3406e4`  
		Last Modified: Tue, 18 Nov 2025 06:15:57 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d849f5d4645b4f9af174911863282198ade83006cab89bdd17f65d3ee298d8`  
		Last Modified: Tue, 18 Nov 2025 06:15:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f87f5fb88be33a9db5251e1ae5c9e1917f0174e83ab903a0c8e3d438643bef70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92046362ba242f9188b9175ffebfee3bfdb89024920b1ad871820dda7742d2e5`

```dockerfile
```

-	Layers:
	-	`sha256:cee639e7a7c11c955a17cc8d99d08fd14d67a9902fd02c86716f561251e2652d`  
		Last Modified: Tue, 18 Nov 2025 07:36:03 GMT  
		Size: 2.7 MB (2680112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6a19143d18661f2a8ea2ad4f2c8ef374615d56d9336636548807b47ac9c2d9`  
		Last Modified: Tue, 18 Nov 2025 07:36:03 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b683e4720e181c392a1e4f2a546fb98be55e86a004caa49290ff0a0267ef3325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141263937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6d6e02ef5aa4039ba8bb7649299121eeb6255af6a90f006362676e33edb430`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:12:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:12:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:12:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:12:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:12:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:12:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:12:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:12:42 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:12:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:12:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:12:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:12:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56b41934afb0543904e93162350649f090c90edf794f96f35e69699407923ca`  
		Last Modified: Tue, 18 Nov 2025 05:13:17 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bc1468af7dc3ff07d4c5e552a74cd81ff782f07e5555bfe38f7d78b3054ebf`  
		Last Modified: Tue, 18 Nov 2025 05:13:08 GMT  
		Size: 17.6 MB (17591054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a009a4c4ec60a39938c3e907090c9b22a81d9bc33c21e09d9822ce4c7cba28e`  
		Last Modified: Tue, 18 Nov 2025 05:13:08 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b33b5142ac993ac2e14efac0de949fa640a1a1dcc95ceebd3cb2842afec1f5f`  
		Last Modified: Tue, 18 Nov 2025 05:13:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdbd7387f1eb6933cb51364639baa2a29bd9b3b42791cff883216e23c6e4015d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7130a17107a8d35ccdc8dd1db081f0d900842a6474f8557c4de292558d1971`

```dockerfile
```

-	Layers:
	-	`sha256:6f9d5ca8c513f272389cd9fcb01cea72aa5b4cd428b2527cea22343c0b86bf54`  
		Last Modified: Tue, 18 Nov 2025 07:36:07 GMT  
		Size: 2.7 MB (2679748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:693875260275b1c52f8cefd042b88c33dbbf061a8f3e829ae2481ef9e614d04c`  
		Last Modified: Tue, 18 Nov 2025 07:36:08 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2980cfcfdc4eebbd67196f141f6c2624d1b61f51303a08159f1490fc22e89a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146157359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeda9848e4dde209349d319ddc6cd8077d8815614f239e0b7762d1ac74af73a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:40:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:40:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:40:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:40:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:40:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:40:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:40:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:40:32 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:40:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:40:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:40:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:40:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a439639461396cfe319eb84b16332b2671db8af4803837382350f840521b8ddd`  
		Last Modified: Tue, 18 Nov 2025 06:41:34 GMT  
		Size: 91.6 MB (91610763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c359a418bf34fc18471c223ff73a38e1fd5b86159b8bb18b54dba442aaa35db`  
		Last Modified: Tue, 18 Nov 2025 06:41:24 GMT  
		Size: 18.0 MB (17959618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcec9a08f74b5451eab271800be332feb04e47a0226b63d50d0fd55e5d11212e`  
		Last Modified: Tue, 18 Nov 2025 06:41:22 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abee1b6155fffcbfeeed40061f8722745c615282d5e3dc2acf041d6953ceea7`  
		Last Modified: Tue, 18 Nov 2025 06:41:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21c61df6c48a361762e00c0363615aa54cd01a124bee3f4426d3ebfe320ad90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e93817bafdddfd16f74ad0760048c32bc54d6872da18f79f518b25199bf9b0c`

```dockerfile
```

-	Layers:
	-	`sha256:2ee740c21e34d504214c990f4ee02bfc3aa5ead63558ac7bc710357d728994d1`  
		Last Modified: Tue, 18 Nov 2025 07:36:12 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec802bdfd48f5e870404ccd56a83c09d89b817c48e862600df4bc0090672abf`  
		Last Modified: Tue, 18 Nov 2025 07:36:12 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:465e94bfd422ee9fa1f7991f4bba331eed7add1ab1266aeebf6bb75f6a021f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137033091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9ac0972da5605a6606573fd780be2acb759af48bd10dfa333f9408b41709a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:31:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:31:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:31:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:31:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:31:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:31:58 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:32:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:32:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:32:10 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:32:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:32:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:32:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:32:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8310960756eddb2cada238790ca1e9b75898eabe6d59a4777d3e84f41140`  
		Last Modified: Tue, 18 Nov 2025 05:32:49 GMT  
		Size: 88.2 MB (88210703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aed124ff7b4851e94143ef2401f527f749dec1e12754dc0894d18e21c006165`  
		Last Modified: Tue, 18 Nov 2025 05:32:44 GMT  
		Size: 17.4 MB (17419823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f2e156e674158f7be6bacad5f9c15d50759a06782c49bd36fd565c267cb710`  
		Last Modified: Tue, 18 Nov 2025 05:32:44 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3550927763f6b7b572246654276fa65b2a0a4893eadd60205cfce5b0353a4f8`  
		Last Modified: Tue, 18 Nov 2025 05:32:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2fffd1f0a8667aba03fddd95065db65b27c3b850b8be8002235e56a918dab96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27042d7cd6d3b077265d51fd6f146e3e212ad0706c03f478494bf8eb3264abf`

```dockerfile
```

-	Layers:
	-	`sha256:5d89b6b015287364107e91fe847f4d03e18df1527b657cab50f694e08fbd161d`  
		Last Modified: Tue, 18 Nov 2025 07:36:16 GMT  
		Size: 2.7 MB (2674474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f334b6ae7f72a1353a5dd0de248d9c614716a771efa4a72a41c0297f1a15cf`  
		Last Modified: Tue, 18 Nov 2025 07:36:16 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
