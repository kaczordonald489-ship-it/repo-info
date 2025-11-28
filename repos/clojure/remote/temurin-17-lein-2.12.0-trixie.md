## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:1171e2ea70abf7256c166c001ac1ab238c140dbb57cf6bb8b3562d2f198b3a7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:135db8dc043c2f9700cbc2a6b416d19948ba6b90998a62c52b9d91482e2a1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217235261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fea86d6411eba4a831577d05d9ac5c11a6efe74ce5b7bb1112327afafde8f62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:09:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:09:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:09:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:09:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:09:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:09:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:09:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:09:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:09:19 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:09:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:09:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:09:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:09:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ff7d3d724f6e7eafa2f958b812d0e14f48504d60fc18d6fa9c346f8781d633`  
		Last Modified: Thu, 20 Nov 2025 03:47:31 GMT  
		Size: 144.8 MB (144847950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6546a00e65c9c3c4eba4f98a00599f3026968d75dd912ecdf9130876dae4b3`  
		Last Modified: Tue, 18 Nov 2025 06:09:50 GMT  
		Size: 18.6 MB (18579632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0128dc3d6affb0c0569eb19196eecd36fd67c088c2e6bd311057c4f22950a2eb`  
		Last Modified: Tue, 18 Nov 2025 06:09:48 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85a3339c66be32ca2d3d5bcf09a8bea38aff64c7fb1a51a9377aa90184bb6cc`  
		Last Modified: Tue, 18 Nov 2025 06:09:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:251b40c3170d942e49fc5a5cefc5658b96986c18ee214385a324a92991d8aa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fd33694d66b9f95c30897e4262ebf6e7e389341c117582e9ba789b2b043af9`

```dockerfile
```

-	Layers:
	-	`sha256:761adfcbf907c9235a5ca5e74d544a5030d56ad8a1ff9b13e167ca76d7ffb446`  
		Last Modified: Tue, 18 Nov 2025 07:42:01 GMT  
		Size: 3.8 MB (3813380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf1159f732be67f41d99852e04c802657da9fec27f13da36d6c43a453034da1`  
		Last Modified: Tue, 18 Nov 2025 07:42:01 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8761bbda6910b9ed2613e1a376fa39cfc313a67ec6201f5525374eb41b5ec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216388875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df2c6203a4b2a3884dd90c2f7ee0f5454223bf08517f3ed61e20ec67dfa5de8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:02:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:02:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:02:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:02:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:02:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:02:41 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:02:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:02:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:02:57 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:02:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:02:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:02:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:02:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f1f030d87697ee7934401a15e97a77f9de614530b0b4e7bfadab067877c10`  
		Last Modified: Thu, 20 Nov 2025 20:29:00 GMT  
		Size: 143.7 MB (143679886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834ea32ae39fe94003fb192e8e221f7b0264315c389922e99fa2b6c59a0d59b5`  
		Last Modified: Tue, 18 Nov 2025 05:03:27 GMT  
		Size: 18.5 MB (18540567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a5db7f96b3f66349f6bb8362a4fffa9f8ef097a01515d53d5af6339b22247b`  
		Last Modified: Tue, 18 Nov 2025 05:03:26 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89475dbb75ceabd4d474720638d88ac970041c1576754a6aea3e387e80b40c7d`  
		Last Modified: Tue, 18 Nov 2025 05:03:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:95c2a8fa45d2d3cbe6f2fb4fd9b66b57c2775b9c2a2837e751c7a3c796c3c132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcbf2e20a3034fdf32d8f18a3e23202cc2ca0c14db79e9a2fb00c95d2de8e57`

```dockerfile
```

-	Layers:
	-	`sha256:c3f8197c5c05b4467a0c415aa5fa2c35ba4181ed15ca51d1dfdc4b25701f78f6`  
		Last Modified: Tue, 18 Nov 2025 07:42:06 GMT  
		Size: 3.8 MB (3814257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c1e3e4820df037040847c3d034354233ed2177567c9c43843b4af324e42220`  
		Last Modified: Tue, 18 Nov 2025 07:42:06 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5f0af4fd83133442ae975b267de14103d10eee6a72f82df4353d25d3ce53022a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220788964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45e44f08d587893890e7b7551f0fe37cc6367a09c975425b7b415959ff9d7de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:27:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:27:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:27:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:27:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:27:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:27:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:28:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:28:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:28:06 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:28:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:28:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:28:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:28:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da80b0b7e9cdabab99dc7af0f635af96aacedb4c191f0957db1f4d6088c8548d`  
		Last Modified: Tue, 18 Nov 2025 06:28:53 GMT  
		Size: 144.5 MB (144525203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d929098c103bce10fff092df423564b8f9d4c76dc62669aae7df8ac3a53ca7`  
		Last Modified: Tue, 18 Nov 2025 06:29:00 GMT  
		Size: 18.6 MB (18637084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11bb091c324c5d3cea5b2a97f20fcf95232d7d7fb9a961d5dff4afd4194af42`  
		Last Modified: Tue, 18 Nov 2025 06:28:59 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c26bbce07e5d0f9bd6d7b19e906763d71d0c0c68b35128af78f4d42f16b412`  
		Last Modified: Tue, 18 Nov 2025 06:28:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4f945ef5d3d1dd0160ab92dfc0c2c784190f937b4045b83ba104e3cb9f55ad9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf55c071b05a745f721a6c8e1f2ec332d0901b0425740f7f2ef9b34949f992d4`

```dockerfile
```

-	Layers:
	-	`sha256:026140550dcf2db738be4151eb7073b77fc7d87f3c334f0de99a2619f6189411`  
		Last Modified: Tue, 18 Nov 2025 07:42:10 GMT  
		Size: 3.8 MB (3814378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c212ae92a9fb3428cbd1c7ca8d16b32797a674e6416a16cf2f0db97063df1660`  
		Last Modified: Tue, 18 Nov 2025 07:42:11 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:68af0e560148e5e1a03f469f4f70295df4b902dfd5d5a253887cb5a99d255b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212710683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820548f8683a3b2853db8e92cd1fa51251a9e3a5200342e9ad36b1ac17f483c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:51:25 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 17:51:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 17:51:25 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 17:52:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 17:52:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 17:52:55 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 17:53:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 17:53:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 17:53:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 17:53:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c945a137e71885488da7cf422518c6c6ad2c6a58a7c3ce93e4735ec87fbd338`  
		Last Modified: Thu, 20 Nov 2025 18:04:59 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a4cf10a12ec4c39807b2ed95dcc39c61ae7483cd6c395fb22bbbab92000e16`  
		Last Modified: Thu, 20 Nov 2025 17:57:33 GMT  
		Size: 18.5 MB (18531695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811cfe0fd366fadf62cecf95bf3616c6968fd7ed29629e1889a268f9e5a29188`  
		Last Modified: Thu, 20 Nov 2025 17:57:31 GMT  
		Size: 4.5 MB (4517810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3d52832eb56647c445ba8d6f9ca3e6c988f51ccbd55790af68d1cf362b00f8`  
		Last Modified: Thu, 20 Nov 2025 17:57:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ffefea93d129369440d70ef9e95bd7d798a1a5ae28dee08d22cb0ac7c9688910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67affc37fc9bf763f853cb51da094dc47aef4fd8490ddffcc7dcacbe20e1311`

```dockerfile
```

-	Layers:
	-	`sha256:a3a5ce68855ae3f64971b10da64943ea57aba186ab73e3566c19402b9d9e6b59`  
		Last Modified: Thu, 20 Nov 2025 19:35:39 GMT  
		Size: 3.8 MB (3801936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c26e480805dd49cb4350ea68f7d4d5ba1fd907fa39edf15cf82c0ebbc9d64c3`  
		Last Modified: Thu, 20 Nov 2025 19:35:40 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3521490bbf12123b46ddbde9dca4b661bb14b8abc42e783f5b91dee1255f128c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207343837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72962626d6f65a1aa7c86753ce5abcad1a36f064bf3a20ee924cdfecc0e2f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:25:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:25:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:25:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:25:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:25:49 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:26:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:26:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:26:04 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:26:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:26:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:26:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:26:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a11b9c90e42947d63125b1586252482ff242a7c5ee2cff882824559dda83f`  
		Last Modified: Tue, 18 Nov 2025 05:26:37 GMT  
		Size: 134.9 MB (134859061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2500bbbd9745476679caa2983dfd4256448ccb4d6d5c5afb454f25d81e8933b5`  
		Last Modified: Tue, 18 Nov 2025 05:26:43 GMT  
		Size: 18.6 MB (18620607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1d991921307018e6e271f6837cbf97be6ac19dd90fac45645d30e03a89a485`  
		Last Modified: Tue, 18 Nov 2025 05:26:42 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a934bb3ea2d5a61fe18d416f53683d2df9b597a3b720cc34443abb8d48be64c8`  
		Last Modified: Tue, 18 Nov 2025 05:26:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:47a877c894903749ec7256399fd17be4b36ae13b31d8b0b6833b8ee80d5c15cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e9deada569a6fc9c65bafaa38bc164617cda806c9e634803b39a31ce023f3b`

```dockerfile
```

-	Layers:
	-	`sha256:f54b4e96ec886892755495d4204bc8f37bc059ec4c8fba78660afbcb4e230e64`  
		Last Modified: Tue, 18 Nov 2025 07:42:18 GMT  
		Size: 3.8 MB (3809807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07ba46239898417d039546296572a489b58987272696da2cfcbac4b7b3ffab4`  
		Last Modified: Tue, 18 Nov 2025 07:42:19 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
