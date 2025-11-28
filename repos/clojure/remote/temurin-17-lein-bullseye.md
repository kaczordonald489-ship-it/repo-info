## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:c5bf563f201ca5be404f519e2688f95d8e5b1c1469f81a15c810fe87acb4853d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:177efe3b89183b39d7932d88a5124e85e787be2ec08cf641d601dbeb581fea05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219730100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e278212fbaefb6059d9af363b81c6f88bffe9fc4fe77e0dcc422d57adfdeb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:08:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:08:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:08:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:08:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:08:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:08:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:08:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:08:33 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:08:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:08:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:08:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:08:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4810deee6e9f42ae37db876faf5a77594f7786f77e340c1618091923748633`  
		Last Modified: Tue, 18 Nov 2025 09:03:10 GMT  
		Size: 144.8 MB (144847950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d515e567018d64d6577722eec79b5eed0fe71cc7b00f2292583082feb0677334`  
		Last Modified: Tue, 18 Nov 2025 06:09:02 GMT  
		Size: 16.6 MB (16607535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46269a19463d5de8496ec2fce869a28b80643628750daaf307c6ab313845026a`  
		Last Modified: Tue, 18 Nov 2025 06:09:02 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb46130ddf185057a3c5a180c0d6ee0ac101deb2860ceb2d5999f75669d35285`  
		Last Modified: Tue, 18 Nov 2025 06:09:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dd600da528984d9b8d84c894c0a4f574a2ffc3a41d78b0dc351082c3140b89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b14fc77f8eca70f8137154d559132f06936176dc818f56f391b6730eeeca01`

```dockerfile
```

-	Layers:
	-	`sha256:ae99d015c692f40b1db8f4cd29cc9a2fa05ec4b0871eaf363259058da43537ff`  
		Last Modified: Tue, 18 Nov 2025 07:41:40 GMT  
		Size: 4.5 MB (4476190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ac65acc2ac083a3c847254bd7a6f3a4036dd525b27e5902a1434741983b82f`  
		Last Modified: Tue, 18 Nov 2025 07:41:41 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:679ce12bb7afc1ef12cdba6c2889144ec65fb14c931fa926ad3502325c30b025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217050794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106c34cadd8424d4ba5c93760babe2a94f967582a856280f871cb9a2097f11ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:01:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:01:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:01:51 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:02:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:02:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:02:04 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:02:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:02:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:02:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:02:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e6a4293c6e1077133e7459b261a3d853cc262e6b190211b27b4ada3bdae4b2`  
		Last Modified: Tue, 18 Nov 2025 09:18:02 GMT  
		Size: 143.7 MB (143679887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9532f31394ef2f6f1d8c383d71548c48a51aad72a29411da235806d773cd4ef`  
		Last Modified: Tue, 18 Nov 2025 05:02:36 GMT  
		Size: 16.6 MB (16595041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5585fbf06f584161b8494359543b383217b39cf9eb3c74845452ed21cb8ca6`  
		Last Modified: Tue, 18 Nov 2025 05:02:35 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f30c8033669e1aba93cf345ae5765de4660e1c0c013574af70408f98d92df51`  
		Last Modified: Tue, 18 Nov 2025 05:02:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:557daf0735e38e2bbb6d28e61678aeb9ec280aa523c88902cc4b7ba643b33f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611acfbff7408f23cd7b3c916ea1a7a7d8277b05542e69929b77977ecae9682c`

```dockerfile
```

-	Layers:
	-	`sha256:01eeb310837d6ea73d6065ca1754501127c46fe018ac666d1806ff1a55f610e6`  
		Last Modified: Tue, 18 Nov 2025 07:41:45 GMT  
		Size: 4.5 MB (4475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba7ae76eb48c7f293c944d82d0694db198adf235f0ee1fa0a7867005b622d67`  
		Last Modified: Tue, 18 Nov 2025 07:41:46 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
