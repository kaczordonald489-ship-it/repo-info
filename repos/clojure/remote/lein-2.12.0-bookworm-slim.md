## `clojure:lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:450c2d160e759be025e0050dc7c300b221cd99e7a34c39f25974c9cb39b5f9ce
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

### `clojure:lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:205b054a58f32183ebf7691c7a8eb501c9085581c055b85623c7836d4cdb12dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142550737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199936cd37a2d6937692943617cbf5d39a91fb95247c43d64b24ad3751c2b11e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:26 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:41 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe45831f0d527879960b8fc7717491ccfa538b21006eeeb8e8702e9e4a6b72`  
		Last Modified: Tue, 03 Feb 2026 03:23:01 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d69bf1cd329a7542680ffcb3c8eaa2e2290c89289d20cb06384a63defb1eb1`  
		Last Modified: Tue, 03 Feb 2026 03:22:59 GMT  
		Size: 17.8 MB (17758819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3e6b8ac55bab4ad1413a0e5b343e327268e734e0ff776e51100ce110d5f076`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 4.5 MB (4517698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5531edee49955baf5632aba79e7fb8d5e4549d7aad2c68661bef0cc98b00369`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44db8c9302aa90d4314e93fe75e48c1103b6e0438e9bc33720587136bcdc491c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68c907a688d7b71e96135d118a02d2ae62ec4e27855b309ed62e193f183e41b`

```dockerfile
```

-	Layers:
	-	`sha256:0500d2668d7d11af5d4e2534702c1c405beda70bb6f1f3e479d0744111627ccd`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 2.7 MB (2680122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a7025131f71f84ae32243e531139a3fbaf6607af7b476f5527f04b5c7631fa`  
		Last Modified: Tue, 03 Feb 2026 03:22:58 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff01219fb491d06660df6ece2dea97cc0f1e674fa9f41a6313dcf710cf41ba9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141270233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f882820975129b2bfc192b3b7608f80038c47c5a41a7ff7cd9b04f087ea4d4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:24:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:24:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:47 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:25:00 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:25:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:25:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc012611b793c22b394f55f8838a6758482860b891bcc239917aba7bad6de4f`  
		Last Modified: Tue, 03 Feb 2026 03:25:20 GMT  
		Size: 91.1 MB (91052508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc796bf7d2e2a9cf944e9b386f84f999250fbf98b311844affab538de943ed8c`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 17.6 MB (17591728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92912bb6a1375b4c7c652c17475a1ea7c893271c146a0add4a26b2f9d00b174d`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f0458f9adccb86e63179751cf74086319e8de258273e9ec77689f337886dd`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec033b398be7c39d3e4db7bb13550c16f967842b88060dc1ecee4a36d6d5e475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcfcea02bb151a449b9c72c1d753490838e59e296cad7d77d16454ecdc32269`

```dockerfile
```

-	Layers:
	-	`sha256:a26d8c065e6b1e87939e130364a0418e637c21d32c9c770eb1902c27ea3a787e`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 2.7 MB (2679758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef1f2d1d3b7b7c7d707f7392c2625a0baf3b04d5a6a4c9b640c1163f3debce6d`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:328bec1055aacb00459745b9ee6fad82377e5759caf41a9f96c9091706eee83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146158381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b93cb00f694876d45f01f49d0c725d9360044e9e442d79f1bd0044460de42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:42:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:42:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:42:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:42:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:42:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:42:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:43:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:43:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:43:27 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:43:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:43:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:43:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:43:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b35e93b96e6ec97e655f2b0ad366e3b2cfef00f6563db06ed66b91aa30cf4`  
		Last Modified: Fri, 16 Jan 2026 03:44:17 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfc42b6a0171c70fe6556b28243e4d819cffb2b8ca83caa8ecd7c66b801c622`  
		Last Modified: Fri, 16 Jan 2026 03:44:13 GMT  
		Size: 18.0 MB (17960731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8309fb5adeecdfc0547095bf708ec7ad24fa1d8d8d30c4a9e4c60b22734b7`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fbe9ba9a4d9708490d42d5c4441f91046f032d2c8dd3feee90311063ac047`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7565e2cf75c11ab2827e4e4f4ae19ebefef95191ea0e65f7f6bb8c592c11e094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d05022736da6d0f55e98cff37e5f38a73a014eb351fa86bbd7cc521d4ab04ab`

```dockerfile
```

-	Layers:
	-	`sha256:dabffd47e903ca7946cfcc0ff815e900816e8f9a7738ba5b0063c6d2dd876f4c`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 2.7 MB (2683265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68861a8f7d5e4b41739b13f2dd018bc43dca1f6162106ee0fcc5c848f56a5afa`  
		Last Modified: Fri, 16 Jan 2026 03:44:12 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fbbccc73f9a144a866f00b072b7ee604e85d044ec774ef973a10a1b6f5ccbdaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137034236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d141402cb44373d5ee3a3649203fae89ecd3acfc0369838bb4999874351961`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:05:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:05:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:05:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:05:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:05:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:05:57 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:06:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:06:08 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:06:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:06:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f3e464ac1afdd462f5598a495c02f0389af1076ca73c693f7f6ddf988c814`  
		Last Modified: Tue, 03 Feb 2026 05:06:32 GMT  
		Size: 88.2 MB (88210676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55df2d6131be3d9e8ae56a3ef2cb20b11fc01ec622e918ccc45f84f9fbd085`  
		Last Modified: Tue, 03 Feb 2026 05:06:31 GMT  
		Size: 17.4 MB (17421038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e118213255fcde5ee87911d423afe42dceb388020a01dff4084fbb6e84bbfff0`  
		Last Modified: Tue, 03 Feb 2026 05:06:31 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1444224307033f9e5077d0864d8e1040f27251e198e0e9a90cbf74490b0900`  
		Last Modified: Tue, 03 Feb 2026 05:06:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fe3e021885a33ce2e1f167efe815ed5dc0607eeb20937f5949e965836911d62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42aae309e1015a18f201c563e68dc585b5c8768f9ed0b005979a1679f34c9286`

```dockerfile
```

-	Layers:
	-	`sha256:45de3ab3ddd380fed38528adcf259996ce18747c84fad875f98e8d0ff00e142d`  
		Last Modified: Tue, 03 Feb 2026 05:06:31 GMT  
		Size: 2.7 MB (2674484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d857f15a4e0beb8979eea7f77faa098c2adc74059a7c3c453fc2e7b89283bc`  
		Last Modified: Tue, 03 Feb 2026 05:06:31 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
