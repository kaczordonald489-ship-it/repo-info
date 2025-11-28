## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:738bdda16e2b2d65e5382b9a72981b43a7e510768235ad7df0fa9700152c7e8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5338313026ade581dcf54dae6b6fb6c51c366ab92dc6b13ddd62fe0f815c06fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194943332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13231dd7e5050d8c563607afbd9887a9d226ad858a40d8e1d824d2ef9186e0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:08:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:08:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:08:42 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:08:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:08:55 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:08:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:08:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:08:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:08:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942e41af9606d4e52ebc963c1411b10bbf96b99df77f0a110298ebb57701884`  
		Last Modified: Thu, 20 Nov 2025 03:38:28 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09c420926bbe858a0ffccf74c85e9767a66f192a6001dcc01195f0057a883e`  
		Last Modified: Tue, 18 Nov 2025 06:09:24 GMT  
		Size: 15.3 MB (15318710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbb24aa0c08e90b0c2bf58f66a4035aae59f87056480bb440106788471e7a2`  
		Last Modified: Tue, 18 Nov 2025 06:09:23 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0a4fbf4e7370aaa08c64b1f91b60e4303ffd3204b6551c80d9f3a6bbd7047f`  
		Last Modified: Tue, 18 Nov 2025 06:09:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce683122d1b1221e8a6a3a52c7760cb127751e20cb0d64bd49df34a6dea599f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c060b51da6cf5c6e1f9fd17c72e37dd84d71c39b66aca2a8e248613fa61100f`

```dockerfile
```

-	Layers:
	-	`sha256:dfff6442e5315fd8d68cf11e6923d3d530062d0dc9916dfdba8cafe10cc1c39d`  
		Last Modified: Tue, 18 Nov 2025 07:41:47 GMT  
		Size: 3.0 MB (3017910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6e2cd7c5753f075efb5004230cd1535f24c8934f7dd3df7c3a7b9af82b3b3e`  
		Last Modified: Tue, 18 Nov 2025 07:41:47 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfc960530ac46d9191ca432fcfe1b3054567aed69e9eb98cb3484b71fcb166f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192252271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82427637ab6a88dde910e7934ede858adb3864a26d2f5d563be0ff931c498f35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:47:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:47:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:47:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 03:47:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:02:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:02:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:02:34 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:02:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:02:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:02:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:02:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1bf7cf8499be72efd862c35e030809d2d6c3b13d9de1bdd76c4bb60eba81f9`  
		Last Modified: Tue, 18 Nov 2025 07:06:52 GMT  
		Size: 143.7 MB (143679884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b2bd53123b549ccc4a1f3c6f74b2a3398180f7e45ddf619d6eaea4cfe1e9f8`  
		Last Modified: Tue, 18 Nov 2025 05:02:56 GMT  
		Size: 15.3 MB (15305777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef25d2f7c9e07d29ac74ffd6a03f797aed7cb18cf8a2ec813ce469af6f03003`  
		Last Modified: Tue, 18 Nov 2025 05:02:54 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6e66474b0f4bd065c0151db847900124ece57dcba5751941a0dcf7f21c70e2`  
		Last Modified: Tue, 18 Nov 2025 05:02:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcfb02ba4a493c9a4e5fa6908bfaa538c003b08a997362620be5421954f5a2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3035242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7eb1b0216e2a273489ff6cc95e66806b400eda6a833c26600a34dd44999e62`

```dockerfile
```

-	Layers:
	-	`sha256:479cea2907bba914a0fda5a04206dbdb11fe3bf182b941df950206913ec2aa52`  
		Last Modified: Tue, 18 Nov 2025 07:41:52 GMT  
		Size: 3.0 MB (3017519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdad7932bb1c753f069a0146819a23dfc132f48e58b7d8ba2fe179b779819c6`  
		Last Modified: Tue, 18 Nov 2025 07:41:53 GMT  
		Size: 17.7 KB (17723 bytes)  
		MIME: application/vnd.in-toto+json
