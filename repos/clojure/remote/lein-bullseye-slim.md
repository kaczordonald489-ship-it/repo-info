## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:d6802444ea5a9a46af57e241d84a138cf6567a1e95855415613c066b25990b01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4c733e6f502e6cb0b5a77d6a2e85c1090bd3627e4d306d1ab3b5af5794a12d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142140705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a7c5de83370ee5e42853a00e56f6edd418467a9d473d0bd90be33d27478e7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:16:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:16:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:16:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:16:04 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:16:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:16:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:16:17 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:16:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:16:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:16:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:16:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85252aabe16b390f678f13c811653627816249a8a7f92e0a8796a38d7e7ed3d1`  
		Last Modified: Tue, 18 Nov 2025 06:16:49 GMT  
		Size: 92.0 MB (92045313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7a5e767a8f48c4e4a35975fd98adf2714405e24948391b94224bc72c10d91b`  
		Last Modified: Tue, 18 Nov 2025 06:16:43 GMT  
		Size: 15.3 MB (15318720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018512b99e03d15d0a5740e7995693a7d6e20ac5c3ab4a50f28b8f8cb2559db`  
		Last Modified: Tue, 18 Nov 2025 06:16:43 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118a78b28080a3df88f8f7b1c4205d04ab42eba1d46cfbce8b06d7014063cd5`  
		Last Modified: Tue, 18 Nov 2025 06:16:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7762614391956bc55378fcc39a687f8388596a722e4ad94d09ce3e8d67cebb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a8d34c38b45acf82e122f2c2c92a786d11fd3daab34294f41373030d349b9d`

```dockerfile
```

-	Layers:
	-	`sha256:b85deccd0f468fc7aab00e484af44361ef9197bea5bec037d2dd50681468204e`  
		Last Modified: Tue, 18 Nov 2025 07:36:17 GMT  
		Size: 3.0 MB (2969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ba61e5db7fa42b45c76015739d11e8ff427e37bc77796cab92cf854cf823f6`  
		Last Modified: Tue, 18 Nov 2025 07:36:18 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b863f68cd1065360a33ed280f41c41466af669277c05fa56ee406914a552aa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139624898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446c2e633a02723df11b4260127bec6355d2269edaf585db218087bdbd183b82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:13:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:13:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:13:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:13:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:13:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:13:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:13:31 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:13:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:13:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:13:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:13:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb35b5a53c49e819271cc9161dc95a3ee8a2bce03037253eeaefa3a7062c192d`  
		Last Modified: Tue, 18 Nov 2025 05:14:17 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1905ec38244bc569cf93c1c1fae8827891189b5a45bd913ce578883ea61d7795`  
		Last Modified: Tue, 18 Nov 2025 05:14:00 GMT  
		Size: 15.3 MB (15305775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cef02a8bb1e6fe2fd5c6994a6c5c1f5b207941a3433f7f735714d21b3c98ba0`  
		Last Modified: Tue, 18 Nov 2025 05:13:59 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dfdb49ace1c715872e17f4a3e16ae3ad9e0e584ce4a00424885457aaaa72c3`  
		Last Modified: Tue, 18 Nov 2025 05:13:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64f6e889c6cc606365b1b883f95209ff08892e99ea09c891ba1f28c24fa980de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be3a7b4d4b0efb4adc8b4a64af542c8feac35fd0c57ec1ea487e14ed1da289a`

```dockerfile
```

-	Layers:
	-	`sha256:b8c3e667dbe91d064b6c8c2c91dbe6d9b92bd200d161a73fc352065e16bf8322`  
		Last Modified: Tue, 18 Nov 2025 07:36:22 GMT  
		Size: 3.0 MB (2968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44d068080eed440237058f2ae1fcd63ae4323558f999877c8783b9ac6a5ca23`  
		Last Modified: Tue, 18 Nov 2025 07:36:23 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json
