## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:105b0129bd08147226a47202417bcf7213e5e1e704719202e98a16fd79314713
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ee2fc335f136e08636a8c8e704702d00028a4a336bfcb79be995ebddefcbb035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195470897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869193d74b320ab2312ee03dcb15b09d4ed77ca29ee4626e081e2c4ed5e6d295`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:07:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:07:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:07:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:07:05 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:07:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:07:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:07:18 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:07:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:07:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2207419dddb167c29d90929006d7657af2addf2aa43de4229d99984fc0418`  
		Last Modified: Tue, 18 Nov 2025 09:55:33 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60133a1f881e47672974f9e493ff40fdc796e887e89c8c1da6a712c99dbdbce`  
		Last Modified: Tue, 18 Nov 2025 06:07:46 GMT  
		Size: 17.8 MB (17758064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7646bd88a1219f6a01640273c495e3b9005afbfdd3ee2b53a8e2bc2633783`  
		Last Modified: Tue, 18 Nov 2025 06:07:45 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea7995486c3bc9f20e88b1a9ea6b1851323cf884cc799e817e0975da45d6b170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd1a01743d0c381738541b46e685df7eb5e8ad03f10f3125b31fac8e349c116`

```dockerfile
```

-	Layers:
	-	`sha256:f33a5aabfd2f44a1943bb66a93289c3a65a1e58ab45ad9dece8d1004e36e90bd`  
		Last Modified: Tue, 18 Nov 2025 07:38:11 GMT  
		Size: 2.7 MB (2748927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5235e1c0d08bf556390ee0754afe61bd479ea7874bd378f1e33ccb28e84dd543`  
		Last Modified: Tue, 18 Nov 2025 07:38:12 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d86ec8fd17951baad81e1d88f6a8fe49956dfe1cdcad74bdba66ce01d1580117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191942643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7d6ebaf72c1d3b95c97eaed7c5602c7d976d67a3caaa81a98f08f3d9035d7a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:56:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:56:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:56:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:56:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:56:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:56:07 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:56:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:56:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:56:21 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:56:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:56:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a668ed7650bbad2b94196d37cdad3ef0530fb6aee9039ebbae7c2fe11e8ee9a`  
		Last Modified: Thu, 20 Nov 2025 21:36:54 GMT  
		Size: 141.7 MB (141731579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c863fd2f399215770eea4cd83a444bef59e60cf21df51dece6b9a5d2ba3a7a7e`  
		Last Modified: Tue, 18 Nov 2025 04:56:49 GMT  
		Size: 17.6 MB (17591069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38370a29a1859cf2405b1b586f9bc583767e53e84d4b7140f4a449be83cf4992`  
		Last Modified: Tue, 18 Nov 2025 04:56:48 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9e1d7206a44fd7c936f46f28c9243f256860ac11634bf74ba2c56162a4373d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0929da27c134b5a62bfe678db8aad6719eabd4b812701798b158b75a5962ed8d`

```dockerfile
```

-	Layers:
	-	`sha256:ac5854b46fbbc91429b85f5b8bca312976330f6caa19ece40e7568177d1df362`  
		Last Modified: Tue, 18 Nov 2025 07:38:15 GMT  
		Size: 2.7 MB (2749160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b940ed2643b0bbf53fb864a5a99b55a7f454e953bf1356505c825b04577ff1b6`  
		Last Modified: Tue, 18 Nov 2025 07:38:16 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:057afd146c450c0a610fb500a5cd99745e7f3c2a7f3828887ad218864d75c3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186628176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c53b4490b94ac5f95c9238e32e14b7d4602cc9cd3afbaaeeb38a99cc3306e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:20:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:20:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:20:28 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:20:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:20:54 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:20:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:20:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb45d70f1a9cc9b98db4aadb38d046c09df2cfca82e5e26482a0ddb0592166f`  
		Last Modified: Tue, 18 Nov 2025 06:21:41 GMT  
		Size: 132.1 MB (132081977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae26db64d1684bdfe03f50b53188a2eb41df9b1bf295b802f6cfc0062d3548`  
		Last Modified: Tue, 18 Nov 2025 06:21:47 GMT  
		Size: 18.0 MB (17959585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8158ff5ccea463502bfc28df2269c5f83ca57d8e65cb98d319b0bb0c28a4cd0`  
		Last Modified: Tue, 18 Nov 2025 06:21:46 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:444341d50fa311cc00ee53ec39bc230f4b8791fa3917ac0a84b69e5015475786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e7e7e6872a9146c79d46ce064723a4fc1bfe44de17fc86245d7073669d4f17`

```dockerfile
```

-	Layers:
	-	`sha256:fb2bdcd08706ed8a2a694ae7545f13079db4ab09c88e6c2f727dfb9eb1e0307d`  
		Last Modified: Tue, 18 Nov 2025 07:38:20 GMT  
		Size: 2.8 MB (2750145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad743930518f292eef674279ef06dbab8f3d33c32059d45902b12f4b050bfbc`  
		Last Modified: Tue, 18 Nov 2025 07:38:21 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ad86581e1872ad9f9616df7d27021f992ae6282ef044b31bf6f50b8cb006170f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174516397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1730b9ed3ddafcc0dd68cc86bd83a5f23da6b0384850e9a15bfef4d20f32cd6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
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
# Tue, 18 Nov 2025 05:23:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:23:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:23:15 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:23:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:23:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1190da05ae19a10b46e3d831eebcdbad7fda228e722f28b4f162aae378b135`  
		Last Modified: Tue, 18 Nov 2025 05:23:45 GMT  
		Size: 125.7 MB (125694433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf44210381ce494214ab283da6ac1b1d1641b34cbf42532686bab71c0ec7c84`  
		Last Modified: Tue, 18 Nov 2025 05:23:45 GMT  
		Size: 17.4 MB (17419784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b64f18eecccca1b25f903ebfd40dabaa7f510565ebb8115edc9ab8dadd685`  
		Last Modified: Tue, 18 Nov 2025 05:23:44 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c226cc4b8a5dd50bcb8518a4de4ad67fa34d88b5be80a43eea6ae82d8b6d3950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db74c9d1b08a51f6dee059de9a5d549409e4e3c8d4b990fc6d7e78a718d336e`

```dockerfile
```

-	Layers:
	-	`sha256:50a9b0a21ed59c0d549d12fdb887ec16fe0ca8a54cf535b70f732743ab64f0de`  
		Last Modified: Tue, 18 Nov 2025 07:38:25 GMT  
		Size: 2.7 MB (2740745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efc7ca4063d7e6ac25f5bfad5a3e72db7cace90ced9c97b1da5445c56f18063`  
		Last Modified: Tue, 18 Nov 2025 07:38:26 GMT  
		Size: 16.4 KB (16411 bytes)  
		MIME: application/vnd.in-toto+json
