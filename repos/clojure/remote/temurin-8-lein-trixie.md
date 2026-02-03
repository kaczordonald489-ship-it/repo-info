## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:09e322d9f184490e92dd836d27c633d2dfa888154df7485ccebf5cc03386464f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c249f13b5f6f49afbfd4436f271a26bd7a9c742086101daaed6b344e8b63a22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127124220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ae485ffefa4df64765a6bd9643b531cf42ad35d2e72ad887bfb28ac520e70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:17:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:18:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:18:08 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:18:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:18:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b4af6dff8f989c4aeed8efe6ef691cc42b8f3ba6179cf9941bed6ccfc3715`  
		Last Modified: Tue, 03 Feb 2026 03:18:24 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7818aac3051d10e9a39a50e4b2c812383d8e59fcb5a05d7a92c7f8ae481b3aba`  
		Last Modified: Tue, 03 Feb 2026 03:18:23 GMT  
		Size: 18.6 MB (18580113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a8c7d3b0fc52f55fbdb1f435895fe7dbd04998863eda22b7713612793828f`  
		Last Modified: Tue, 03 Feb 2026 03:18:22 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bdeda3d9e875c85f2f23899a86659476ebf85f6718ad98ca530646a8aa4296e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c1f3b01c864488a10a1f5cac6e52756f76d295b75ef28f1206efd822c368ac`

```dockerfile
```

-	Layers:
	-	`sha256:1398f9b64a5176b3326a37bc853b32eb64ba08d5e4cb453d01b4a8680a3a8171`  
		Last Modified: Tue, 03 Feb 2026 03:18:22 GMT  
		Size: 3.9 MB (3935849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7152e39788f6a402d957435c3f0c2db381655c5fc6544d6496b9971f59fcdc65`  
		Last Modified: Tue, 03 Feb 2026 03:18:22 GMT  
		Size: 16.4 KB (16351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1d9f32a9e907fe4509c60346d8f5e8c5406944dd57b6983dc9ac190e8a9651c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126526227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b02207abd9290253225fe8c066d9a276799346499ae1d6d61ab6bdebb5c91e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:37 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:53 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af47a74ca157a80cb50f146f406aa388fd1008d63f47e7bc0328b05e1ec19f57`  
		Last Modified: Tue, 03 Feb 2026 03:21:09 GMT  
		Size: 53.8 MB (53814975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e792c2b66b7787d010a003949dea1589fa0c2deba2cf0f9d8d00642cda6c984d`  
		Last Modified: Tue, 03 Feb 2026 03:21:08 GMT  
		Size: 18.5 MB (18541446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2451b35931acf0149681255e9b95fc52cbe3741c2e674dfec52e251d488f8342`  
		Last Modified: Tue, 03 Feb 2026 03:21:07 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:925a6e0d876af2ad35689989eec199f88c644a6d3c39b4e59c69e7ecb3c1dae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4604c4b186ebdd2014dcb3f466834763d934812e495c99c95f0f285952d8e29a`

```dockerfile
```

-	Layers:
	-	`sha256:bd597143911a355de208f957c54a8f87273b2d16268899f4a3d11e0bfa7e61f1`  
		Last Modified: Tue, 03 Feb 2026 03:21:07 GMT  
		Size: 3.9 MB (3937424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd3bcb5708f0c37b987fd9e6e3ea739fea1fbfddbf15a90221ac6a0246afcbd`  
		Last Modified: Tue, 03 Feb 2026 03:21:07 GMT  
		Size: 16.5 KB (16472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:665aa333d2c6fe2b889bf87bc6374abea1f47a5d49467f814a76a4285442ea49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128437082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141de3c2fcc6a9fe48273951dbc5677bd6d7935653012518fc355a51f55fa7f4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:48:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:48:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:48:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:48:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:48:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:48:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:49:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:49:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:49:30 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:49:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:49:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b450c5f7d58a9a7ac9c8651b6b73ac9e1c6307f2834881a528832693d6211e`  
		Last Modified: Fri, 16 Jan 2026 02:50:15 GMT  
		Size: 52.2 MB (52175110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3d4f5f53a63734346bc51c46466ec649e3eda27959e83aab47e9897499b206`  
		Last Modified: Fri, 16 Jan 2026 02:50:14 GMT  
		Size: 18.6 MB (18637246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf2e2dd6ec1bfc75bd33105f151c024f942356946d52eae01f120ea1e0c55`  
		Last Modified: Fri, 16 Jan 2026 02:50:13 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f9c80485c029668a047d25d385dae10d625ae46282bf7f54f5592b50c9999f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408bc90aa501278da790ef9b7dcbe61cc1411c19c2ace7f526e4765829821cf4`

```dockerfile
```

-	Layers:
	-	`sha256:d694e40427614887fec7a0541362ec3773fa2dfb01e360caba89eac76f507745`  
		Last Modified: Fri, 16 Jan 2026 02:50:13 GMT  
		Size: 3.9 MB (3937442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd7827e7a3b3c9a63dbb2ab0d8526f0a6ceb2feb7cc6a596ead7d413d2ab244`  
		Last Modified: Fri, 16 Jan 2026 02:50:13 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
