## `clojure:temurin-8-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:195faf53fe49949904c659bf05909f7e2ef4df3ee4e6489621d3825f120eebb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2189439fbf5d19e415cc27cc671faa4945d330dd7f7f1e7ca98670b4c1b0e4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129615123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f489e85b73cd1d7dc7e017bc1bcaeef9fcb93502a536338e2db931a4eb514764`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:04:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:04:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:04:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:04:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:04:39 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:04:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:04:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:04:53 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:04:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:04:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff5fb1c89d41a37e3bd03e87680d4442df21085731fb80000d0338bf0dea4e`  
		Last Modified: Tue, 18 Nov 2025 06:05:21 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc504658f99b4829c18c5d8bd73b8415e92c9576d976f2f3a0a2fb556ffa735d`  
		Last Modified: Tue, 18 Nov 2025 06:05:17 GMT  
		Size: 16.6 MB (16607522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9b7d9373857bee3fa5b17a27976d6807aacf36101802a61f155d29ec0bed2`  
		Last Modified: Tue, 18 Nov 2025 06:05:15 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8f22b4782c78569c21ccb8096fc5efe0cd38d2dd6bd44833b1f7c324c001ebd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4614170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4612e6bb1e122a1cdb4449071ccc3e0022f5d1cbd0c9d82f8af1c8bf23b8cf`

```dockerfile
```

-	Layers:
	-	`sha256:62f56185b51db060c9b312050ddbbf45717ed2803b4d7ea292e4c08f418dc31f`  
		Last Modified: Tue, 18 Nov 2025 07:50:18 GMT  
		Size: 4.6 MB (4597800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0637a6e4beeb2b7deb98fe8bc136d1c8609f7d5dca18bda9994ae8780a13e3b9`  
		Last Modified: Tue, 18 Nov 2025 07:50:19 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdbd137503612a6f896570195563741a1e19494e521e7791c394582a4ed72330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127185514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24086aa3f2dfe55747a844799ad9d64c0965d050c2ce91f425a81e9502f3ece4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:50:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:50:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:50:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:50:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:50:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:50:43 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:50:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:50:56 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:50:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:50:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae4a24ec95cabc81c07ee511c849e694be8864186f5a060bbb45280f8442b1`  
		Last Modified: Tue, 18 Nov 2025 04:51:31 GMT  
		Size: 53.8 MB (53814999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbc6d1baafd82eaa72ed14983fb0d368a68e15c17ac3b2f4ee39fe9509b18d`  
		Last Modified: Tue, 18 Nov 2025 04:51:20 GMT  
		Size: 16.6 MB (16595040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36b032e05eb84c0a9c46760364e1b350c3ba82d2ebe4fb84097a3b40e5e60b8`  
		Last Modified: Tue, 18 Nov 2025 04:51:19 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:55a9696db1744e74c24ec4a3727f5ddc626580cc553f5cee9f5ba60a745bffbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4613963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d4f8afae973545541ff8a61bf9bb6f3057c02cb6bef4abd6126a287ea28e6d`

```dockerfile
```

-	Layers:
	-	`sha256:3401c33c29979d85544fd68a8fb40108e21780043d833b0ebcbb33e2b53bb33b`  
		Last Modified: Tue, 18 Nov 2025 07:50:23 GMT  
		Size: 4.6 MB (4597472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c8ffbd1a196b4f4ca0c93c80869c406f28e1be58296ad48ba075c41e6f00880`  
		Last Modified: Tue, 18 Nov 2025 07:50:24 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json
