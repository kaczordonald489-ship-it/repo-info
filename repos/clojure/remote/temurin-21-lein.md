## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:0735c23336769849d4e37e55db45cdf8f95acbedf278e252534ab9fea22f5a4f
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

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:8a8cc210505bbc0763af53331a58b620bfd3899db9be29d79c417d1e681dd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230627740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6309f5b92bf312d3e2968d25eacab1a1ecc1930834791675deee817e72b807a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:11:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:11:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:11:29 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:11:44 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:11:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e1d0e492652a26dadd3edce733469157fbece64ed1760dff07fb2c63640f0`  
		Last Modified: Tue, 18 Nov 2025 08:35:36 GMT  
		Size: 157.8 MB (157825966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f05eb6ba786ac55e9ee15c42052f715f121ba152e07fa9ab00aee47d3e25235`  
		Last Modified: Tue, 18 Nov 2025 06:12:16 GMT  
		Size: 19.8 MB (19802836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4a6353c7f8d7f0581f1edb888432f21d66b0dcb54e44dc295043032a997e3`  
		Last Modified: Tue, 18 Nov 2025 06:12:13 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfed211c983da38cc8a787c5f2a5aa9a9ffa3a86c8a862a2064d736fdbf270f3`  
		Last Modified: Tue, 18 Nov 2025 06:12:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:b5f73f09ae800b580e1db838fb3c42c88280ca0211c56be4741ddb0a92abebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e049409bf18d3496c6ebc02159566c6dedaa617d5b6410a2d342deb95fc8254b`

```dockerfile
```

-	Layers:
	-	`sha256:02bbf1ab99d45c8ecaf6bd331f6742608197efd04a10360ff45fc5da3fa5512d`  
		Last Modified: Tue, 18 Nov 2025 07:44:25 GMT  
		Size: 4.3 MB (4283588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad0edd30065f75f7fb5e8366b58d42dafe891b46809fa807f2e2250937fd2ae`  
		Last Modified: Tue, 18 Nov 2025 07:44:26 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e30fb14b7da8c1c08a091d1b1ccd767cf4f204bd690dcd09067c486ad3ada9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228616987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da095446cf1ef2f2ae307f9d7e6ae62e8ae3a7bd98fa8d0531bd8211febd70c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:05:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:05:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:05:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:05:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:05:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:05:59 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:06:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:06:13 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:06:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:06:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b6d96bf738eca8f099272f0e47e6aadd0613f9b79a6e927ee36d2076338f9c`  
		Last Modified: Tue, 18 Nov 2025 12:07:38 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238926e48e2018b8b69d002cb4216af0ac25e8b07ec3eedba6adbde778bd4182`  
		Last Modified: Tue, 18 Nov 2025 05:06:51 GMT  
		Size: 19.6 MB (19632125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1fe86d5b725b9e2e5faae6f88d8185e9d70668990c471340be2d55c5697ec`  
		Last Modified: Tue, 18 Nov 2025 05:06:45 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b151d6e4899bd2e66575f39db9ee42c3c1e376f93d8cee2534b56b888076166`  
		Last Modified: Tue, 18 Nov 2025 05:06:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:bee175ec9562ed15db76dec2d3a0cc2d989232adab241be9144f8844faf03600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52213ddf2162656bced73afe86d718d2cd53c092843b790091ccb6e0c6aaa90a`

```dockerfile
```

-	Layers:
	-	`sha256:dbdc31975aaf59c41c3bc01bbe93daa9c50cbfc6ae8e961d3773095fc9f193ac`  
		Last Modified: Tue, 18 Nov 2025 07:44:31 GMT  
		Size: 4.3 MB (4283227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a804c3742f0aaabe49361426dbb0561d8f74571aa6585c0f3181edd64c5efc6`  
		Last Modified: Tue, 18 Nov 2025 07:44:31 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:111d3be7a437d2ff74eb764d6514b3905271d9984b0f1d9ebd3d8bf6cc67e206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234809852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fe4d495656c82af31e3db993766fb4b788b577b9ea986a8163fd326061f06c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:31:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:31:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:31:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:31:45 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:32:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:32:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:32:28 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:32:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:32:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:32:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:32:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d206fc81389c537bf3bf40e30bcd9d24259322fc1603ad6f79f10d5009db2a`  
		Last Modified: Tue, 18 Nov 2025 08:05:04 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39b613bab4181d6f31b666413ff0c2ee9d66920fb74dcd2ec09e373af197883`  
		Last Modified: Tue, 18 Nov 2025 06:33:53 GMT  
		Size: 20.0 MB (20021764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc213bc68a5b95a63d2451874910135dac846d5deaf7a9b86f3add489b3ab7be`  
		Last Modified: Tue, 18 Nov 2025 06:33:52 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53a691584d66d015203f6e57a6cd9b309809f804426e8dcefd2d5ecae48925e`  
		Last Modified: Tue, 18 Nov 2025 06:33:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:5381d5c8b6929542af522ce2b6aba172eacc98b3e04434407f9b8ee534487a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb3e1082e5153ba1c4e6f53ee64f0460c0fbcf77e9f9046925f719705a0997`

```dockerfile
```

-	Layers:
	-	`sha256:93be78366ab0ba2d5525756191b592e8551033a082857e38aa34de3297f361df`  
		Last Modified: Tue, 18 Nov 2025 07:44:37 GMT  
		Size: 4.3 MB (4285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731df97b4e07a49ece38f1036f0774fc96fff2c5e326f1d9afcb6e3fa83dd39d`  
		Last Modified: Tue, 18 Nov 2025 07:44:38 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; s390x

```console
$ docker pull clojure@sha256:f4f39d7b97a4c0f3aa6dbade1000cde79dd0837e8457872bb18d28f3f53a3a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218186421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d33eebae9cdf222e8d549773511d4d52d14deb70eea3227d921df7a50a749ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:27:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:27:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:27:33 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:28:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:28:14 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:28:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:28:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:28:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:28:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a4c2d7559d27df7dde4cd8b1f0f676863b5a0c885adc1250cf0bad409e4500`  
		Last Modified: Tue, 18 Nov 2025 08:05:38 GMT  
		Size: 147.1 MB (147069839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24be45f571847ad14a35cb00c56382a44e4e4fd842df07513b615d69aa57c1`  
		Last Modified: Tue, 18 Nov 2025 05:28:52 GMT  
		Size: 19.5 MB (19460766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8807f4e313768f2cec418c8b35d1714bf93d85d99316445597c2683db34fa`  
		Last Modified: Tue, 18 Nov 2025 05:28:51 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32195df45fc5471795b1719a8d34846d05dd4c64acdd3ea35950f19ee177df`  
		Last Modified: Tue, 18 Nov 2025 05:28:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:cf6dfcf3b891894ebb39c78739a1c4365bb1f7beb448269e12fe8dcc3772b546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9dc91b66a2548a0f22d82c48ce2d2fa83b78b9e956b47755b3d091c12af7ad`

```dockerfile
```

-	Layers:
	-	`sha256:76f745968e046b9cfe7fe80f4a9f2ab337b21ed307a06ac561cd0b5af6b71061`  
		Last Modified: Tue, 18 Nov 2025 07:44:43 GMT  
		Size: 4.3 MB (4275402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:290f34c225c09aa69c9e1be4f4e8246cc8451592f8c7485ac732a9642f845791`  
		Last Modified: Tue, 18 Nov 2025 07:44:43 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
