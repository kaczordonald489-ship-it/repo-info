## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:841912b6b27b322a83c762d91fad6720d84a7b18c81e299035f6d995dee1c855
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ffb79f3b79399849ad337a487016c507559492902bdc90293d2f84f78a942f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208330611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0d8d4692b9bc41ea8ef0cd0fbf792b91dd23f4138c349fd5f03860d7652dc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:12:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:12:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:12:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:12:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:12:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:12:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:12:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:12:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:12:18 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:12:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:12:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:12:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:12:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120dc18a8c8f6234b4b23471adb6f31897bdfbbb30aa8ceedfa3afeab0917cc`  
		Last Modified: Tue, 18 Nov 2025 22:46:44 GMT  
		Size: 157.8 MB (157825974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02516eaa3ff682a7dcabe494e3711a80e09d48b2991e298f1e6f84475530e277`  
		Last Modified: Tue, 18 Nov 2025 06:12:49 GMT  
		Size: 17.8 MB (17758042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf31c2901f415d077367cef0f20422f8708c1ef5d5730feefe511b49f85b846`  
		Last Modified: Tue, 18 Nov 2025 06:12:48 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5905b382b62e41135aca3c842cf44ff592c95c61a35f3f67b0a79e8230a4`  
		Last Modified: Tue, 18 Nov 2025 06:12:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27aaff4a59ca989a3458de718698594ca940f2c8ccd4a64588841cd4fd776b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43fda30f8de1e8d9076a57bd322d95ed72bc7c5eb0cf71c3fc26e3e5e665644`

```dockerfile
```

-	Layers:
	-	`sha256:e979727f8e2a68bd6ec96cf7c9af127a1a12618ce996d67a048f43bbcab12385`  
		Last Modified: Tue, 18 Nov 2025 07:44:44 GMT  
		Size: 2.7 MB (2731890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c900a44b6b064b7f21904e672210537af5fc137987f37b207f087d32fa1c72fc`  
		Last Modified: Tue, 18 Nov 2025 07:44:45 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc8815b65bbffea05c0f9995526731e3b58835726518967365c2556cdfd01a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206319178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7081326a7eb3b9a8c5254b4a8f1cf0f806143b0a7b732f14f232ca2d2c794e5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:06:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:06:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:06:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:06:21 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:06:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:06:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:06:34 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:06:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:06:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:06:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:06:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6945169938d8af13555e63860e059ef3ab728c9d5916b9233eacec06c97c17`  
		Last Modified: Tue, 18 Nov 2025 14:30:54 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153a4447dff855fbb387ef5c948f084e8f89cae6411f7d49e8bf8c31d6f87e26`  
		Last Modified: Tue, 18 Nov 2025 05:07:03 GMT  
		Size: 17.6 MB (17591117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a637043130cf11a3015c621bed924e941acddec04b6906ad2bff9baefb8bdb`  
		Last Modified: Tue, 18 Nov 2025 05:07:02 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecadf8ffbd18a30d24942ec5d149e67336f50cce550314cf4570bd14c41be29f`  
		Last Modified: Tue, 18 Nov 2025 05:07:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8ba315847a8aeb52ec2b452e19a46daa3caf3fc9cd0814c444a9f3b99abd5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fca87dc38588068ace81e02e29fc1f04fc48bcda35d8e88405535973c12f7f`

```dockerfile
```

-	Layers:
	-	`sha256:657a4d30d317b67e74e166ba09dde7df700b087c66410a573a69427761d9f786`  
		Last Modified: Tue, 18 Nov 2025 07:44:50 GMT  
		Size: 2.7 MB (2731505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50093b8ff841e7864046af374d9f59b353dab96368ac0a7d677e3fc24bc3a6dc`  
		Last Modified: Tue, 18 Nov 2025 07:44:50 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:83b78f2b730b3f33eae990d2e61985e548e303967ca018fa66bc68aec22e5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac4075cf55618d217e39a2c39aecde1ca65f7ac94e24d2446679d30a1959e53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:34:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:34:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:34:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:34:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:34:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:34:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:35:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:35:07 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:35:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:35:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:35:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974478515d7c186335e22d66c2a7dde61bca42ba9c7978f9a54fbf628ade7ca`  
		Last Modified: Tue, 18 Nov 2025 08:02:48 GMT  
		Size: 157.9 MB (157942922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae626b50b5cfa3667c10a4c8f6dde8ee0140f3a11161bbe9238c17963b489f`  
		Last Modified: Tue, 18 Nov 2025 06:36:25 GMT  
		Size: 18.0 MB (17959691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd93d7df6ca06affcad3db245666606fc57925965c84cf0571f5a6ac69e3f543`  
		Last Modified: Tue, 18 Nov 2025 06:36:24 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdf58cd3205cf54daeb66dbb354dbc38b9a1be86b6e96c14d9ad89736bc8adc`  
		Last Modified: Tue, 18 Nov 2025 06:36:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b41fa23e89a3e6c2d56ac5f8dfdc3475a1a8c096e881f991e214f3bd93e57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae2f7856cb38be9be701780f71d40a8fea7fa0a23879bc8867be30195adeb58`

```dockerfile
```

-	Layers:
	-	`sha256:42655b47b520a3e56463e177c9a4d23e66daf7a9e1061a03d9aa419015b704b2`  
		Last Modified: Tue, 18 Nov 2025 07:44:54 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d880ad42a5a313288e6d5ef811d347d7da9c82b13a4e46762fee6130aeccd90`  
		Last Modified: Tue, 18 Nov 2025 07:44:55 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:58ad668428a4da14dfcada3cec5ce43debc3990bf7482eb4f38dccd286e2b029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195892168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aefd18020a74629cc196e1b1ceae16a6868bc6a9b9e689e28b542c7028d4e93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:29:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:29:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:29:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:29:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:29:10 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:29:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:29:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:29:20 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:29:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:29:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:29:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:29:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415602b41fe29f565cb6f40bc115c3f7a4f54bc07ed4e0df0facd0f20103746`  
		Last Modified: Tue, 18 Nov 2025 08:03:21 GMT  
		Size: 147.1 MB (147069811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c7bdaf035538a2a466809f54662d949acd57ecba8fbd9b152dcaabeda3dda`  
		Last Modified: Tue, 18 Nov 2025 05:29:58 GMT  
		Size: 17.4 MB (17419795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926fe2d313a8a1e7addaa2cd1307be434ab9b9d1263e2eefdc1c6b3e75689c43`  
		Last Modified: Tue, 18 Nov 2025 05:29:57 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a1271404bd727cd7a5bf96f2c69b6ec2c22b9829424cc2105c64682b7d0e5`  
		Last Modified: Tue, 18 Nov 2025 05:29:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a82f226960e6589874e95f835e8987559d53320a41f7371d66d22f77a8693fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b8cb999b54fd6a01e22ef20f60970d0627439b2ffd91871ca7ca781c4822e0`

```dockerfile
```

-	Layers:
	-	`sha256:31963ea1ea5ff93f64ab91a1ee41caacb7fa6ee30e1b4c43598a4e763fe74fb3`  
		Last Modified: Tue, 18 Nov 2025 07:44:59 GMT  
		Size: 2.7 MB (2723704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682f4146d2ed68ddc7cc237fc4cb2a633f85153d2fbca9b9f0daa691dcb8d47d`  
		Last Modified: Tue, 18 Nov 2025 07:44:59 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
