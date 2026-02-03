## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:aece1b9602a659414b6c8eca2f5a7f0f28df1045eb327ef51ff7a491396b25c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e8914c82550e63e9efab5b142c8b9886888efd1984605a2edc3a4f8206c5c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194943052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c833af9bfba3d59245bb335fe36d85f53bfc1b5a370e3ccb3ef393ce3cbdfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:20 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:34 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf6d6cb3555cf374b8a09a171ce43706e83f88bfa269672bee4b898004ac22`  
		Last Modified: Tue, 03 Feb 2026 03:20:54 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788d44406e302923a39924130f75f6abbdaa043e51fa67f61e15dd7a6208b277`  
		Last Modified: Tue, 03 Feb 2026 03:20:51 GMT  
		Size: 15.3 MB (15318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebd85e84356d32690b5bdbcff9658ad57a3a23111017e59a3ee5c3cc617c6b1`  
		Last Modified: Tue, 03 Feb 2026 03:20:51 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75923c67db26e92308bc84d7568750da1e7972f6e530735339469fd2e0255e28`  
		Last Modified: Tue, 03 Feb 2026 03:20:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70b11e6b819621e9fd04d0356f1240366c6fa5f3255f0eaa8ed3fa6cf9e41062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d135f855537f12d6f3c65178a8ebc12d8cec16a0fb85bcfab77f76888f4462`

```dockerfile
```

-	Layers:
	-	`sha256:79ae2c581f06413caab849b56efe7f45cec407a6fdf8a5a4e9c83d39772f0141`  
		Last Modified: Tue, 03 Feb 2026 03:20:50 GMT  
		Size: 3.0 MB (3017910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ce0dd608b9b527c1f5a32660fe70a1ca03efa6ef6d2346a525b049a0dce5f3`  
		Last Modified: Tue, 03 Feb 2026 03:20:50 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7097e5e7a3398ff30e24de50cb446a2b56b2a0d59121f45d7a5fd6d74ba29e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192248331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af11765a4980e252a7f0d2097b3429ea9e74a74ca440e66b8f7c5b9cafd0783`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:23:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:02 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:16 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac78f6bc6ed8ddc2a94061babaae407e1c615cc8d08ecfec607b7f166b8a1301`  
		Last Modified: Tue, 03 Feb 2026 03:23:38 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161716b44f1b278f0d371fb189344d2037d20b53d3df826059256cb41d284bca`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 15.3 MB (15305767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2411a56c1f559177a38a8f0b67111d801d1c75d16768daeda7743b5ca16b7b1f`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02328d2f443e32d310abf089da052319ba1d5155912cad223e88b1e99e7df471`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a661c2784066cdcc51e08ad4daf507acf261764036bb5000ec59bfa486c445ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae47cba1f11811acd24cd9a75902d7f6b5773e7b31a0d583369c87768770f4f1`

```dockerfile
```

-	Layers:
	-	`sha256:693ebf4d506e42052c1e772230f3a08852b04b9ec2a9a13fa6eff7d1b430c84a`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 3.0 MB (3017519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce7598b8ac513c2107e5867449321699a8ba3c5818968db54a84a7b2885571f`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
