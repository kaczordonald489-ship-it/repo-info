## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:0c95331eb8c6dec1a2458cf33eed802e8dc9d3a78bd439215e266b35f36d776c
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:37a4d370c96ca698dabe0cbba6bf7abbd3c261f31adcbfbcf7f2cabf98e82956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de811e5652607b62078a4ac558595e9c6ebef8f7e5ad5539dcf9db75b9fa6be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:15:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:15:08 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:15:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:15:22 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:15:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:15:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:15:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:15:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967d4c66b508c207d0657091dbfc4f9b9edca63e8f88dc9b986f4a89a1667e0f`  
		Last Modified: Tue, 18 Nov 2025 06:15:55 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a9dc72b97685586e5c1b40925913383253c7d04103d49b05b1cd134957267f`  
		Last Modified: Tue, 18 Nov 2025 06:15:50 GMT  
		Size: 19.8 MB (19802944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befa6667a7a9cd2e18e842e3667c5ff05a68a1c712d6737b37671611a5086b89`  
		Last Modified: Tue, 18 Nov 2025 06:15:49 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239523c768cc210f50a6e61a2e27be19f8af50970a80ebc2c539eea0c2a87842`  
		Last Modified: Tue, 18 Nov 2025 06:15:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d1c4d25447bcc529bddf0c60f371a9c464fb19fd9d4dbd24de898a6a83865199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e934c6cf824572ab8571b1ada4bfbe10a7ed5258269b56308e59c420093c05`

```dockerfile
```

-	Layers:
	-	`sha256:f58deb2fa0093b9c43eaf297de709111e9f0e5897ce4c24c5292af8386099d0f`  
		Last Modified: Tue, 18 Nov 2025 07:35:42 GMT  
		Size: 4.2 MB (4232396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f89f76045bee1af607a72f0af4cb31641b4eacdf3baaf4164c32a6cbb131623`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa8b65809aa9b0e070a3a6e39a7e74519c3d2e32e02e681fac1614c193cf9873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163561933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b29514b2b174f9c5195679f0c03cacc52392093f268cb05470294cac4e6cb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:12:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:12:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:12:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:12:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:12:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:12:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:12:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:12:15 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:12:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:12:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:12:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:12:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c205f6f704aedd7b44f180f1d4fdb4baa335a7feb723463afef939f491f333`  
		Last Modified: Tue, 18 Nov 2025 05:12:53 GMT  
		Size: 91.1 MB (91052529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7343092cca6cf74e0cc6100291fe7e4bd0a41d44de6a3d1071f705ed13a26060`  
		Last Modified: Tue, 18 Nov 2025 05:12:49 GMT  
		Size: 19.6 MB (19632125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b92d516eed09f9c3aa3de57c994ebb21884ef99fb1f5f6660db5e83a0a284f`  
		Last Modified: Tue, 18 Nov 2025 05:12:46 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56f37557268adb7cc191bc0b90f0093c2a8e61dd6c5b4b525a5c841be3d1e9`  
		Last Modified: Tue, 18 Nov 2025 05:12:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:effa6a6462aab5ea75d5bc260d01be2ddb7f6de8f66315dfc89fbffbc46e3a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f1400b37b98f2d3bea5efe176f865cccb0b95fe8779a0c84d7a4d03920dc49`

```dockerfile
```

-	Layers:
	-	`sha256:5809e9a81794f48cd796e2702cd428b3bf13177266960fefe844ca5ea4f35411`  
		Last Modified: Tue, 18 Nov 2025 07:35:47 GMT  
		Size: 4.2 MB (4232080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1e3ca3af02c2ff4c3d4c70953a3f7228bd577fc82121ccb0901277fada9984`  
		Last Modified: Tue, 18 Nov 2025 07:35:48 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b2a112cabc63a98dd102c16b101037c0bbb46bc021aac638af4276f1cf5aeaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168477560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a784049f5d7373afe2fbe5d8cfb29ec988350503b7cb8122f9ce9a1c5832f50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:11:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:11:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:11:07 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:11:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:11:40 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:11:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:39:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:39:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:39:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42c99d7c799ee7cb4bcd9f016e2e075ba0305357c43f87c1b2db5156bd271d`  
		Last Modified: Tue, 18 Nov 2025 06:13:38 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d544d7e2ca975664c5aedb6a3c6df31c6420e2af3582810953a088eae6d5ff07`  
		Last Modified: Tue, 18 Nov 2025 06:13:31 GMT  
		Size: 20.0 MB (20021612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc751a37c12c4f7d4cf63db767bcc33cb0c18a1a1e811cd40ac357771f88cba`  
		Last Modified: Tue, 18 Nov 2025 06:13:29 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc0b048e69af17fca2ef22ce76009f2b7248d04cb785c57204031e0cd3a087`  
		Last Modified: Tue, 18 Nov 2025 06:39:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ff438651856ab0cf1a8feec09ade6c6d79e5a07824c366b5989be9e5577370cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eada02f600948bd6bc983540e01a4c2eea0852b7823bb9f4046a0c1e2f695475`

```dockerfile
```

-	Layers:
	-	`sha256:d13142a2b03a64e4c9959e71be06fcc7feed46b69ddab19da1ca88c454cfdbc3`  
		Last Modified: Tue, 18 Nov 2025 07:35:55 GMT  
		Size: 4.2 MB (4235589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d3b4e2186e0c205ff207eedfd352582a374de5d73ddedc47c3748fb71ab6c9`  
		Last Modified: Tue, 18 Nov 2025 07:35:56 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0a7f1905a179607bac4a3d3620eb43c036b757afeea8ff724b7e1cc82b4c569d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159327295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193a7a8ecdcfdec009731f8bca0cf5f4cb72d87c326c9162ccc59af53beec02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:21:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:21:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:21:07 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:21:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:21:16 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:21:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:31:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:31:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:31:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa22c8373b8566c846a7e580361bbb86bc05dc4c1fd3498c8de8ba025ecfb1b0`  
		Last Modified: Tue, 18 Nov 2025 05:22:11 GMT  
		Size: 88.2 MB (88210740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e270a59c4ae54170eb18c7e8ad6bc0df7908096a95c2ef80742aeb24c4b8c`  
		Last Modified: Tue, 18 Nov 2025 05:22:07 GMT  
		Size: 19.5 MB (19460725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53200e2cf02a4d25011b2e6837c04c28ceb7cb6aedbd7dcff3412b0a39f1e1a`  
		Last Modified: Tue, 18 Nov 2025 05:22:05 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5fe3dc8d41ad902ad55588c3c1628937264b47d46f1de71789f608f6c48a1`  
		Last Modified: Tue, 18 Nov 2025 05:31:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c74e74a812936492c1cf87578ada002c4048e7f922fbf7d9b3c67fa9d783313a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a348c5d40e5b1d10a7e7a20fffec29c0b0525c81fcba32e442fb0a9c07cc2621`

```dockerfile
```

-	Layers:
	-	`sha256:12c11ad6c906104e69596564584b33fdf8759f93d31d6c497e843b0ce3c1baea`  
		Last Modified: Tue, 18 Nov 2025 07:35:59 GMT  
		Size: 4.2 MB (4226758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e34dd1f350b2454af44a44a328663a118ae3b718fc4dade82c92dbe07fb38b`  
		Last Modified: Tue, 18 Nov 2025 07:36:00 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
