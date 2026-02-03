## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:faf2f30a711d00050c3b1bea6938bf37529428ed0ad6c91b51fdabac5d0fb414
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6a6f73b69a72ec390a25f7084b9b1c15cd412937b5290568f21150bd195d48a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142789267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299bb5d72746e545e167dd882fd16dc2bad9772d50f2c1f872a287daf4d0d121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:38 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:56 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b56121e607a6c68d1d272940fb2dc4f926a318cb0cca259239f057601bed1`  
		Last Modified: Tue, 03 Feb 2026 03:23:17 GMT  
		Size: 92.0 MB (92045315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a6b4c246fea9b181d81e30c115f5c73c648090aa049035fbd0dc2b81b2088b`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 16.4 MB (16447189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcf785d1501fdef48557f90b1c9654c5c52a696caf30e6935aacdac0260ff79`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af0c20888f896f3d7639c4cae78f45e8547e2610ce65a43d5cdbe4ad0e5dd85`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22146376c82f14dbe295ce0290b56aacf66d269f883a4be309d64c65da1bc9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390f0e221fcb2f8518633fdf646fc0c66cd7cc628605a9790f8715508d514c5b`

```dockerfile
```

-	Layers:
	-	`sha256:61c8c14c0b715395dddc8408beb191428391f9c7f106eec34f99015266deebfe`  
		Last Modified: Tue, 03 Feb 2026 03:23:14 GMT  
		Size: 2.3 MB (2314816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e6746735ba3b22c9eab14ccd611b7534c1ced2e52b96799cbf46161a9f378f`  
		Last Modified: Tue, 03 Feb 2026 03:23:14 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df0e45c82f4f21a146cd2141be38d190cc7d3a5211905eef6d213e08acdfd19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142124314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3594d0a08251799b95a1dbf6cd008792ab7ea4710fd90fde74e37f32844e013e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:25:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:25:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:25:08 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:25:26 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:25:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f0d9cd75a1a8aba9a83982a31bda92a3c8f69269a8d76466c7c3f255fe1d6`  
		Last Modified: Tue, 03 Feb 2026 03:25:43 GMT  
		Size: 91.1 MB (91052474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71675c0025b00b33af5ae78d5ac2f377dc054e534f5960182c2e58e24003cfae`  
		Last Modified: Tue, 03 Feb 2026 03:25:44 GMT  
		Size: 16.4 MB (16413603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef21a4724eb7d7ce6458539cbcc7680a18f83218be2d5bf7d79301ef5e20fad2`  
		Last Modified: Tue, 03 Feb 2026 03:25:44 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be43543a39574b88ed68070362079d23afe965eca3e844d453c258e64a8edff`  
		Last Modified: Tue, 03 Feb 2026 03:25:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0dfa25c36909b15a1197795899377f15c75e175c4b5610ef6e0d7af288f25f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a3c6875ac370fc41465f250443ed1e9b7eca1f1bdcac845b2bc9e383bb6663`

```dockerfile
```

-	Layers:
	-	`sha256:738b726392a3d34bf97cf59cbc0e0768eb960507a13e246e6d3fb956fa85e863`  
		Last Modified: Tue, 03 Feb 2026 03:25:43 GMT  
		Size: 2.3 MB (2314455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eea6d06e7132755531dc85e34d1ed2f8b72b6c43ef7ca79adf7507b06b075b`  
		Last Modified: Tue, 03 Feb 2026 03:25:43 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c9219c8c142a1f110e08a2f9c781eda4aee38ffc6d5ab3b0e0efe6ceb6cb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146210004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207d080d615907ac0a31e731db4db1057d3a6626c41518950bd189096f1dd0db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:44:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:44:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:45:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:45:58 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:46:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:46:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:46:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11e063d257c7fd0378d1844308cea571e43cdc3c6ef2206a9db6629a1520ee`  
		Last Modified: Fri, 16 Jan 2026 03:46:44 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246e2006158f66cdaa3bace84b646348ea88497a12fefad6e2ebd992dc5fa6c`  
		Last Modified: Fri, 16 Jan 2026 03:46:41 GMT  
		Size: 16.5 MB (16485502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00af45bdef0f7e5ee487d595115ee9c3d4330035bc8f19f7b51331818da304d9`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb0817dc0f0ea743dc97f2d9291c0bb28bf08badba082482f92dc1fc050569`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b03653d35b146d75d7dd06769461aef8ee5a80f6e3436b72b921cbf6a984b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc75237e4a804dffbe74f8429b97d875639aade17bb62f3c4e5a0d2eab236db9`

```dockerfile
```

-	Layers:
	-	`sha256:199b4e9e19ae0d738a6c50d273c8b28f10d00bcd9eb61b19c2915c276d4f0ff0`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 2.3 MB (2317106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3854a295dd88b74e952f2154ea5ed5fb21c5c6a97d819acd313f80b009a7289`  
		Last Modified: Fri, 16 Jan 2026 03:46:39 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c071188e15d65f57b091b11939a14f7cbf37011183c0b6758955a66d8e2d5180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139940677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162aefd4fb798fea6f94a8ee7553a870ef6904d4ab925a97da9fb3db19c7c479`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:35:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 04:35:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 04:35:54 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:37:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 04:37:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 04:37:24 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 04:37:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 04:37:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:37:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:37:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c69cdd71ef06850eefda28596d4212304f3101cd9d101f44fb4cf0c74701f3`  
		Last Modified: Thu, 22 Jan 2026 04:41:12 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d432eb238e252eac4cee820a5bdcb5eca9693a30f0babf3f179d068bb4f2726`  
		Last Modified: Thu, 22 Jan 2026 04:41:00 GMT  
		Size: 16.4 MB (16397877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2121be5332f7e06e8c00c5175080fb8b025a018dbaeb30dd5ee9ccbdc828d39`  
		Last Modified: Thu, 22 Jan 2026 04:40:57 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ffc66d7d3fecb7172637ad501c824a0fc4b8375d98787ff7efc7e794b2fd3`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de1992eebb3b0cf68dc70398d9768e59d2e660667c7665f9cc39e5314910e106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ccc05f86b1e8007fd9689c051402e9f948a47f600e07ddc81a29c609bce066`

```dockerfile
```

-	Layers:
	-	`sha256:05f77c833a41453c4e21d93caf444b679340b477e9050ec62cf4e13a045e97be`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 2.3 MB (2306873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880b4f1e61032268ebaef8ce26a06bb9550c656ae6b5c12935eea93b99fe70c9`  
		Last Modified: Thu, 22 Jan 2026 04:40:55 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d3d6aefb6960a50ef49da15e561ace6d8c1bb38b649ec840b4605cc7a3a17eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139050385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4825ee21e5850e537a4e63849ffd3175d04df1db77c1686ae4726d8097e12d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:06:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:06:27 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:06:39 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:06:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:06:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f4900007f98e7f67419952a5a5a7cfdb2468fd30b472fb66d39a7f43c9064`  
		Last Modified: Tue, 03 Feb 2026 05:07:05 GMT  
		Size: 88.2 MB (88210676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb25e7b91743604f5b5195d674cd59abbdd32c5e01febf68fff69d61f17a3`  
		Last Modified: Tue, 03 Feb 2026 05:07:04 GMT  
		Size: 16.5 MB (16483382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed61eb112818f009b218605f6dfcc9cd906de5e198ae6e448db542b5249eee9`  
		Last Modified: Tue, 03 Feb 2026 05:07:03 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d48be475a4d67678b2ce10553de57104f6c9332977e81938f268d60597a01`  
		Last Modified: Tue, 03 Feb 2026 05:07:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8df9dea10f76ed02a1d8d75f98b180d39a48f45bea455f8b0836eb7e9cd0e40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c7c1939dbb3eabd41496f46184fc98d9de1253933f3e0d9624075a9342db7b`

```dockerfile
```

-	Layers:
	-	`sha256:f6669c318c9aacf05b7df6ed8ceee85c1b7ef4da47a88ff3272d1471d39bddef`  
		Last Modified: Tue, 03 Feb 2026 05:07:03 GMT  
		Size: 2.3 MB (2313791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70558163d36ef1921b867527f8c02db03331505bb845ffd27d652ade0a7e9df`  
		Last Modified: Tue, 03 Feb 2026 05:07:03 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
