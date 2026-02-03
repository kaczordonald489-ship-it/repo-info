## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:256bc14258126c2236a932e7e66bf721b39517aa1a8c918b5e2c6e948f2ccf3e
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
$ docker pull clojure@sha256:abd708af570b1bee8dc04b4fd2f228e8a03a0b73b91a691da27ab19947045769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208331441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c732a6a0d95bd1f2fdf41045374860f4962aaf21d6e034383ce97836896578d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:21:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:08 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:08 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:22 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872149c40563950cd34a5ae3ab9ba85256f64a5ce87e77d6168ca1ceb8110614`  
		Last Modified: Tue, 03 Feb 2026 03:21:42 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed5498284db00d3e0dc403d7690831ba35fa65d127348acb854438fe40003c7`  
		Last Modified: Tue, 03 Feb 2026 03:21:40 GMT  
		Size: 17.8 MB (17758781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ad0c05996243326c81f8e1bedb3cc8cfb806bb1a89404affa84c5142d8a9b2`  
		Last Modified: Tue, 03 Feb 2026 03:21:39 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9390c87db0945f59b5137b7c77641e372a5f120bc13c51b4ee11b1577b2a0fb`  
		Last Modified: Tue, 03 Feb 2026 03:21:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33ac2e7bd4327d5e8a35fe91a92ba339c19b6eb68f4f5acf707c145e65e7650a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059cbc4fb3eaac0409039e577fd0cb82d9965562deae988e88cd2fda248f6b4`

```dockerfile
```

-	Layers:
	-	`sha256:1a35137ff2a3bd2b1673ccf4aad89bf2e2a352fe2551f668c11570adb21bfb57`  
		Last Modified: Tue, 03 Feb 2026 03:21:39 GMT  
		Size: 2.7 MB (2731900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72fd77ef7750808d523fba35fd9a15a3184b472b71fa4f259f5e1637575dbba7`  
		Last Modified: Tue, 03 Feb 2026 03:21:39 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:669d1d6a2916f04e7c97e91f63ea4a8a00dc6062b13945434cf53ee50cef0669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206325330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2576fd8dba1e97308d1d5a6c390123213bbdfeb6ce5b451d9867d91dde26ac9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:23:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:52 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:52 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76e95a29927a8441ee12e5f0e5ee34abd687bc6bea70e31c628dca462c34841`  
		Last Modified: Tue, 03 Feb 2026 03:24:29 GMT  
		Size: 156.1 MB (156107653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a1954e303e63c783687b8b4a31953d3eecf7df1abc68a692d14ef2f6f6c92`  
		Last Modified: Tue, 03 Feb 2026 03:24:27 GMT  
		Size: 17.6 MB (17591733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a5e20184b95e339815a49e4a3cc2e9469aed3169d73e842a4245bc7ee0f565`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 4.5 MB (4517692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9deebc73ca46a4a8865775a4eda4cac23d22c26bc7510e16f1eb443ac35627`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d7e756d2cc9b87e2d1840c423c831d9c067a4130bdbed751b4a473da50d1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bb2179f0ed20e94ef6da915941e67dacd32f5ad9d5c1b2292400684150a179`

```dockerfile
```

-	Layers:
	-	`sha256:f78f358f503c87e3a2c73cb640d2230ab32b7092cac403db4feaf20e4de3c6f6`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 2.7 MB (2731515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201e09ec4aa92bebdc4ea32c02517039729d8e80f9f916d28af49c9ee3e8721d`  
		Last Modified: Tue, 03 Feb 2026 03:24:26 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cad4fa43770c9512424b27ca2bb5559b4eb345bfb6cdb9105090ba919acac926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212490534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded14f2a34906e9e7ad344a6d8c653d9b8123fb8d93c87a71b29357349397091`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:28:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:28:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:28:00 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:28:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:28:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:28:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:28:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094bf46310c703a83629a08ef35e481705d22cf663c8418d08e57c629ca01ea`  
		Last Modified: Fri, 16 Jan 2026 03:29:07 GMT  
		Size: 157.9 MB (157942940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751c535fc5f2ea89485d9c3ca465484ec68e7092770a2a102f224cef03fc1709`  
		Last Modified: Fri, 16 Jan 2026 03:29:03 GMT  
		Size: 18.0 MB (17960713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64a286216efccb318efaab875e47bc0571342ebb9338276600c7688e967e58`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334abf4bc4d45281691abe56bacc265b1bf49ad819b9311553f2701012638e3c`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:149ab5bca0691d188d6f8b2697fa7145c44667e2ac8371b6c7863e97f65d1ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2af23a053823a2a99c89dbe216e28f6f9f74303f703d32a1f94d6ea1c8368`

```dockerfile
```

-	Layers:
	-	`sha256:f479b9b956b80ab198046a7c2b4e58621f8bf90c3be741e4e5091ed45ea3a05f`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 2.7 MB (2733733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eefed54fc6c6bf7636b43f21042dc205e891caf68447e957c715b1aff2c2324`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9fbbde54e53d9944802e219f84c7c540e348a96d1ab87b8709c96eb3fbb447ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195893528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d62cf9d0c6362dc3c0a4909e82ba87598b0b9df47fed2893fcc05502d0f7197`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:03:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:03:53 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:04:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:04:04 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:04:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:04:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ae753e080cc50ca20884f34f16a7a103d8cdee0bb115b2a6163947581cac7`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 147.1 MB (147069863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0b0ee8c41e6ba864a11e1936dac5b45761498f2d84d5b89482c4d4462586e`  
		Last Modified: Tue, 03 Feb 2026 05:04:31 GMT  
		Size: 17.4 MB (17421112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a806d1233485d5235f6cbd3c28ab5a1d2bebe906cd3b58a676004897652bd71`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d913490cd2d5717d3ffe095c96cb571b1699fed868e1be879da8245dc2d5d684`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1eb496e282b564ea0a56ee6a127f7bd1e867c7be117a766fbe9492378eff891a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29455ce26756d8c5db04465428ac1ad9a5dd8382751951bb313f45f163af3887`

```dockerfile
```

-	Layers:
	-	`sha256:b2e46d91c4b1c24a8f2d67b5e84d050a2891624433e6fbb564aa705ebf1f967e`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 2.7 MB (2723714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e5fb41bb8108476d9260f037376e97f998840bd85ddfea028e118e8ea73ca2`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
