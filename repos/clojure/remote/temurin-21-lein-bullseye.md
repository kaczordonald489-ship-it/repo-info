## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:f4faeeb815d503f8efb2dff7a37b1ce1cf6183d021961b1d5883570dd2e8b1f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0460e6ec815e9e44f635b3deb1f938db91143df4dc38ddc0183556d9af9fbdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232708111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfb6867a0bf284c667387d5a24056d35ca405fb2040806299d3b60f4db8d4b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:12:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:12:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:12:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:12:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:12:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:12:09 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:12:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:12:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:12:23 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:12:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:12:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:12:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:12:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de2ad40df06433cc5a6c27157ccfba1bcb6a743e0cdffd70323f8f5ceae845`  
		Last Modified: Tue, 18 Nov 2025 09:01:55 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4195affd580b7a504e047e94cb0a258121d68981bfb0c3ccf5c4b649cd8a3c0`  
		Last Modified: Tue, 18 Nov 2025 06:12:52 GMT  
		Size: 16.6 MB (16607570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3937189f427f4cc8393b2e8b0312648039c3a5801f195500012f9ab67b718e`  
		Last Modified: Tue, 18 Nov 2025 06:12:51 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4169b5be2d1a2d97e22d9d49a749a8305e11b599d2570b765f174b12640224`  
		Last Modified: Tue, 18 Nov 2025 06:12:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:39e72c34c4e74c4feec1bdd58a0cd7fd5d4df79d295e8bb0fb35a8a5d611792c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287d92b57dcf87a1b96b64802912ed761096cb5fe789dd52d04572965f5dc343`

```dockerfile
```

-	Layers:
	-	`sha256:e9254c38bac36af76770bf11b447595ed680d8e5156dcabfc2cf4ff6d79de4ce`  
		Last Modified: Tue, 18 Nov 2025 07:44:53 GMT  
		Size: 4.5 MB (4479292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2095bee6b1bb119f3040987d4570af887b55e1a63309cb3e8bb7db971ad1d31c`  
		Last Modified: Tue, 18 Nov 2025 07:44:53 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6c2a816f14f2f1db4a5d4333b596a17053f356321bc016f7c903a485eeaf1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229478421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a78583904f97b663ea45bffe7db0fe66c5479a067ed4b0095555d43b9061ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:07:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:07:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:07:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:07:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:07:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:07:14 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:07:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:07:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:07:28 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:07:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:07:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:07:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:07:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1d4e808cb2f8608fbd40f2cae5a592e308fe9eab5fd45c92bc5b05e5136c78`  
		Last Modified: Tue, 18 Nov 2025 09:18:17 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00173c070a886367fb0196ef192e2c6043a025cf06939434d8aa6066b9dca2a4`  
		Last Modified: Tue, 18 Nov 2025 05:08:00 GMT  
		Size: 16.6 MB (16595001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0d1f0d416ff3c8ff2c86371b48fd29edbdebf26e05d50fef8332d04ab414e8`  
		Last Modified: Tue, 18 Nov 2025 05:07:59 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d129fde468e391e78c9e51693ded541862a1922bcb8ec550abe2141de691e`  
		Last Modified: Tue, 18 Nov 2025 05:07:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cec6879ec18829e9ad00e0ed8bdb7f73973a1604c41c1a92e6a0e775def660b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d59515cf117d440e65a5919b9b8b7996165fefa93a59a8ba9c2c5730f49f1ad`

```dockerfile
```

-	Layers:
	-	`sha256:a20821b0a377db04d1f25ea4f9ba49110848d7ef7ff712ee5b1ea7df4433f32a`  
		Last Modified: Tue, 18 Nov 2025 07:44:58 GMT  
		Size: 4.5 MB (4478266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ad3dda3a9104d7a82ba6f0226ad191fda4b546e88bb1a62114bef9fe8cdbc5`  
		Last Modified: Tue, 18 Nov 2025 07:44:59 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
