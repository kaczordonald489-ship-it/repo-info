## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:9dd3017951fd2a8e0fb43739bbe39dd66f14e9dab834c551089aa5e301a172e2
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
$ docker pull clojure@sha256:e97f95cdea5328c586e473bb68d28cece8787cc42f38f1d2b3a06fa7024c7e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dd3a7a428bcd590a7d3893fc7cb38cfeb86041b59758b979a15cf5a95aa7e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:15 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:15 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:17:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:17:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:17:31 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:17:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881678cd63841dd6b8330c52c04cbf408e8458eb009c9e276219b07b29a5bb2f`  
		Last Modified: Tue, 03 Feb 2026 03:18:11 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa46f66c956280b195f9695a63082fa00b694d7700d18963c0e232bd14991`  
		Last Modified: Tue, 03 Feb 2026 03:18:08 GMT  
		Size: 19.8 MB (19802869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb33a8eb106e3985a10efd8454ecc1b3384c110b648b9f835ac8762fcebfa19`  
		Last Modified: Tue, 03 Feb 2026 03:18:07 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b09217b59d11d627627a1d853a017b15567609e976af48efeff1a78570236c5`  
		Last Modified: Tue, 03 Feb 2026 03:22:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e559bb093d94b3e94adda07d5a92b9a985680af8ded1da380ebe40ae153be696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b32a79ef944d8340de8668d62043bd86d427550674d6a40ff0f5d89086d7485`

```dockerfile
```

-	Layers:
	-	`sha256:e733f30cbd9caf2c02fe5293d01f9c46a28dad4ac723686cbb4d688e2825949b`  
		Last Modified: Tue, 03 Feb 2026 03:22:17 GMT  
		Size: 4.2 MB (4233039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7020c09b4ad38324308f70d4ec4749c508ce4cbdb2df51b5b5f5190f76abbef`  
		Last Modified: Tue, 03 Feb 2026 03:22:17 GMT  
		Size: 19.5 KB (19460 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b2bccea465c6f0188aa71801a24e70110e49f41b90294ae3359f0870c0f5866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163569365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecc9c2c2eef1708ea8ce739d262e4d6cf6cb5333e7114c2a0df999d698e68fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:24:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:24:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:42 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:56 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e756ff880c80b0f446d17789d6d71383d40ee3d604971b115b78f9ee722b60`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 91.1 MB (91052484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea90f8017e08d1dd1a0a60bfeb34ce24fec1e291c687d6f5f878448fc8cb8ead`  
		Last Modified: Tue, 03 Feb 2026 03:25:16 GMT  
		Size: 19.6 MB (19632785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b774fa17a3b0f8f6c01bf27ce78762aa8d7b14e21627c7b075b1e6cf11c13d9f`  
		Last Modified: Tue, 03 Feb 2026 03:25:15 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448f16301d3d78fd36752829a921a8e2ca1ca1164ed2d3a27fee5920a1259885`  
		Last Modified: Tue, 03 Feb 2026 03:25:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:16096bda21b86b56e478f9af3b71672b492870076501249f04798794ebda90c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb98139b48d3a9c036307b6578eba498c426b41150b63c3b52d2a366c46f1600`

```dockerfile
```

-	Layers:
	-	`sha256:6e3a45c52a455649f9700aee0c1353f9e867d19fd60c91ce7ccfa45e583f7ddb`  
		Last Modified: Tue, 03 Feb 2026 03:25:15 GMT  
		Size: 4.2 MB (4232723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee39ddd86ee8f6f3aa176f5919c06823bce694db43f624df4df15c3392407cc4`  
		Last Modified: Tue, 03 Feb 2026 03:25:15 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba30b9dd4328e3bce836b304e9bb9c4ca608dbda822ca06e014fc42d1d2b1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfa84eebce07fd4ecfe5f86a13d2255021d9118f82e4b2d2b8e42be3943ecd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:43:19 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:43:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:43:19 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:44:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:44:05 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:44:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:42:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:42:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:42:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a2bd88573c70d41d7945da863a10fbc76252e0180def2eb63f3e259f7f1fe`  
		Last Modified: Fri, 16 Jan 2026 02:45:52 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c1135f98921991ae84772c0a37916fb368af39e47c22694bf0d3645512503`  
		Last Modified: Fri, 16 Jan 2026 02:45:49 GMT  
		Size: 20.0 MB (20022500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caf94f89bf158a1e26bca0e2b0bc88a465abc44e79b816fc7248dc275efdfa`  
		Last Modified: Fri, 16 Jan 2026 02:45:48 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07e18eeaf2f582ed94d300b69b9b650fa1e5535d475c8b8177ab019bcc7ac1e`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ee3a41ed1817aea73efc60eca0b67552f8cd6de370ded92bf0265101c80b2a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce34bed38a2727327dc6be725300801a42ab2c095daa33761eebcc2362cc2448`

```dockerfile
```

-	Layers:
	-	`sha256:a2947bdfa6059759e29f2861d4608e722d4be4b08f660902701f6be382e7e6fb`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 4.2 MB (4236234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a64f2b34a398675d7480157859250ec2ac19c6418117479cac1f153cbf9287`  
		Last Modified: Fri, 16 Jan 2026 03:43:01 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a592f4633811679a4039bc952f9109e01db7405e7444d2b2056197393e10de20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159330360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ad2e89552e280697b517943f3d87190d29524a781db0580285a3ed27447907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 04:59:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 04:59:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 04:59:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 04:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 04:59:42 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 04:59:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:05:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdef57afedce759031aec2d24c0fff4c7e6f222a37d2f21fec7f3a9fa7818efe`  
		Last Modified: Tue, 03 Feb 2026 05:00:27 GMT  
		Size: 88.2 MB (88210680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dcaa56ef88ade0a292848fc88fdf40a42d022a832819281d71aca24b922530`  
		Last Modified: Tue, 03 Feb 2026 05:00:25 GMT  
		Size: 19.5 MB (19463171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1368acbdc7a6eaab11c831e35adaeab66006541b564334b620ad19ac5039993`  
		Last Modified: Tue, 03 Feb 2026 05:00:25 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908b7a800edbfda8296167bdb23e7753ab12212bbac3d8356d295416c903b004`  
		Last Modified: Tue, 03 Feb 2026 05:06:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79a4a8944764eead7b2e91d1063570f08f4b62d446cc1715937d5e7bf5c5e24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93088142c5292744386de174941108b3ec4999fbb7cddfda8304f882bda8fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:8c3a19bb76e13f22a7936bb979f2359986f30617dd7797040d65555d14c95636`  
		Last Modified: Tue, 03 Feb 2026 05:06:10 GMT  
		Size: 4.2 MB (4227401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd8ba77238e8274f44efec7c2e7aac637f3f260183c970187777b21b75bc796`  
		Last Modified: Tue, 03 Feb 2026 05:06:10 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
