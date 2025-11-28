## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:be0d05ae45428da1e2c844518b288aa6e80ab62d3eed2cf4614a796668fa2d83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74b028fd2f2bebc291d0ce81fc4b7f1848e9e1ec474302d33a25b5d768f4cc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105474784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96037cf7119f883527fd80f8fd961a4db9138de2cd3bef920da674ffb2f0d1f8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:05:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:05:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:05:21 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:05:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:05:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:05:36 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:05:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:05:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630edd71fe56932bc2ebb15f6034cbf5774be33a4a56f4cb2481150a7762851`  
		Last Modified: Tue, 18 Nov 2025 06:06:02 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e841526b830d605a50bd8b4e94132f9e62ae3da8a82166207fab4ae43b5163`  
		Last Modified: Tue, 18 Nov 2025 06:05:59 GMT  
		Size: 16.4 MB (16447125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460b5ef8fac4c112e7c403583f7d5e8a8e47fc15adfb8beda7a7a59aab5ffdfe`  
		Last Modified: Tue, 18 Nov 2025 06:05:58 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4c45405cb7130f2fdb86ade1a31c79bf6bcdd3ea9b260e377a67b9f03453e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d53084f4ac85975ef73756f56228090dea63eb58a6ff4563e06f27e40a58eec`

```dockerfile
```

-	Layers:
	-	`sha256:5f663fd27e39226844d1dcaeed0f0a44316f2704b30e27bdca5767c762073b69`  
		Last Modified: Tue, 18 Nov 2025 07:50:44 GMT  
		Size: 2.5 MB (2485048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa089311905e8bd1ca332d5f7848244fa7c86873374d4a8572be63e8d884fe75`  
		Last Modified: Tue, 18 Nov 2025 07:50:44 GMT  
		Size: 16.4 KB (16381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7cc1c430d4239f9e4501ffbb4eb54ad95c3c3cd225914323113186ecad9e5ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104885199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da236367979ab0417bb0c30e7e24dc9a065efb72c530302f201e8f68795650f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:52:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:52:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:52:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:52:03 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:52:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:52:03 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:52:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:52:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:52:19 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:52:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:52:21 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e10a9eb6b78d78f061af57796b8721d75fba9dfe4142d6b2400b3a36c4e61b`  
		Last Modified: Tue, 18 Nov 2025 04:52:47 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd4d191572b3fc0cb244fd5819e78852fdfe996d4ddd7afee5615633f972be2`  
		Last Modified: Tue, 18 Nov 2025 04:52:41 GMT  
		Size: 16.4 MB (16413837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c4ee32d8318d0ae3dfa2e75d53871330d3750d3d50018e60cb12cbaab56805`  
		Last Modified: Tue, 18 Nov 2025 04:52:40 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8295d5bca79f3cb05106b82afeb7d06158971b79156f87cc1bc8bd3083d0a512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86c649ee12ac9fe64f1e93ee54823cf01c4862ee92f4e0ebe3b326d0e205306`

```dockerfile
```

-	Layers:
	-	`sha256:cef11f1198d00791375dccf4ca92d3e5511da51e852ecfc0c2518f433e4bfbc1`  
		Last Modified: Tue, 18 Nov 2025 07:50:48 GMT  
		Size: 2.5 MB (2485364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38d9ba4f8adf5d2beb95e37bc8c70520170b0bbf2a0c331b59c0808334ea82f5`  
		Last Modified: Tue, 18 Nov 2025 07:50:49 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:31314f72eec8b6c2e9a3ed3475c071e20cdfd03753cd56d8404f367f6c53fe71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106774984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1c6f9feb314564d34d6c4916bf4aaa1c305ab4956886a0b957bc390cd6fb0f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:00:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:00:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:00:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:00:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 19 Nov 2025 01:00:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 19 Nov 2025 01:00:01 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:00:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 19 Nov 2025 01:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 19 Nov 2025 01:00:33 GMT
ENV LEIN_ROOT=1
# Wed, 19 Nov 2025 01:00:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 19 Nov 2025 01:00:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71419e9ee2bd73ee8f94b7448e68f7185a7bb5e2552828526f349e1c2af2ff7d`  
		Last Modified: Wed, 19 Nov 2025 01:01:37 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8dc24d7fe78a05d80bdf851064f2dacd2170414122fe38ea4d3e194b7d8db`  
		Last Modified: Wed, 19 Nov 2025 01:01:34 GMT  
		Size: 16.5 MB (16485169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b119cd99c80fe9fb1f5f279ab00b595813dc6c1223579eb55da4905f04747213`  
		Last Modified: Wed, 19 Nov 2025 01:01:33 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d293395c5bb139cab2fd1c3cb2f13d2684f4dde90f3bc6eb509ad042d194ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608f1924d92f6c74eb1b0d2e40f0bd802f96559a4c64eb537fcc4e0b0a2e42f2`

```dockerfile
```

-	Layers:
	-	`sha256:21987413a32218903d256a3821ca7d827d24aa808e7c810a7366a6db3a280796`  
		Last Modified: Wed, 19 Nov 2025 01:37:12 GMT  
		Size: 2.5 MB (2486621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fde18331161a61d099515e68c67d6c9cad14247a3ddca1d96223b3fa4e0d4c2`  
		Last Modified: Wed, 19 Nov 2025 01:37:14 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
