## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:5b4fb271193d08ca5ffc085f5a214999d7996aa0c435f221bf40e4188f211af9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd5248ed41bcd3557b28cc9d0f511c1fbf2c3761b493ac4110797b5e7e6ddb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142140462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594b17698fff5cd3af48cfa38a2aeca0ee6374cbd7896c604a6725e133928ef0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:46 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2885566194d02922e1aacd38b0071631f2407f70ca0eebb74564cee3ecc5d2ac`  
		Last Modified: Tue, 03 Feb 2026 03:23:06 GMT  
		Size: 92.0 MB (92045330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47a6a710a29206b77ed56fdef7760c74bee848ad27111e611dec96caf2a83d1`  
		Last Modified: Tue, 03 Feb 2026 03:23:04 GMT  
		Size: 15.3 MB (15318674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3413d3196cd2b8fecc2bc006e347a7b93692dee82fb9631b8e183bc1c011c0d9`  
		Last Modified: Tue, 03 Feb 2026 03:23:04 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c03de6d70960e949f30d2350c8624c2753665f1f64f70cd36a2f02f8c85253`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a0b91e69155c8db86dbd151e5588b99fd1796975e669209d0a8284ff4af8879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97488ec3bda606018ace1589fdd047085ecb0d5291d5c660dd824cfbe9c4f005`

```dockerfile
```

-	Layers:
	-	`sha256:3740e21fe7a6bbb74833d8fa11f8bd019a99d772271593de5d9ec00a279e4adc`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 3.0 MB (2969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33da9bc73bff0ece6010a0760028627e1f65e7ea7badbac5976820e263936a37`  
		Last Modified: Tue, 03 Feb 2026 03:23:03 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29a2dd954dbbf78e1d0e1203b30e9996f668a3cbc5f8ea489352492306c0ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139620831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ed9d23c40d554feece39e8969cacb26695c7afec1e7e0bff178c014082bec6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:25:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:25:09 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:25:23 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:25:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f0d9cd75a1a8aba9a83982a31bda92a3c8f69269a8d76466c7c3f255fe1d6`  
		Last Modified: Tue, 03 Feb 2026 03:25:43 GMT  
		Size: 91.1 MB (91052474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6602113e2f4a0d56051d3bc802936d179eb46b46cf99f30eeaa8e4fdbe0efd1`  
		Last Modified: Tue, 03 Feb 2026 03:25:42 GMT  
		Size: 15.3 MB (15305780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55a2dc25a7169fdd6dee4df22119409b44bbd622fe13acfc1303ea4c979207`  
		Last Modified: Tue, 03 Feb 2026 03:25:41 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b95ea02a17a058d048751a831c232fd2836461e53e2a8397a6f042e90e0c48`  
		Last Modified: Tue, 03 Feb 2026 03:25:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc1c5d1bd7986135a880a63bd2d621361ab88e93cdc9ae062acb2df5f2f84449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86531d5eb3381ad5f1b4cedc9624a31fed84821ab78a9a2adeb6bf1bb1e80966`

```dockerfile
```

-	Layers:
	-	`sha256:9eba138d2b995ebe9932f05e7bdfea25c3ef5815504afce02edfa435a3b1f73b`  
		Last Modified: Tue, 03 Feb 2026 03:25:41 GMT  
		Size: 3.0 MB (2968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82f26b75f665597f8386debe1a817ca95d3ba294b81c39f381310ea87321454`  
		Last Modified: Tue, 03 Feb 2026 03:25:41 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
