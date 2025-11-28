## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:703cd982f93ae2e9dba0fd80a1c02f864a9434d4e0d11efc4845a65efc6adf39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:96a629c7c6f7df1da5561a7d690621860451b79d9c13c1d47dfc93f87078caf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47622d5b13ecd1cbc3ef91aee66229274add8b2b518c0663058f07f9ffad6840`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:05:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:05:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:05:12 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:05:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:05:25 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:05:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:05:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154ca13844bf3fc1369ab8f81d6b1c627106373131a35c8dda5b09b02f302e8`  
		Last Modified: Tue, 18 Nov 2025 06:05:51 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a434a34abc2e361a1f3f5ea1ea7d7942fe789c5dba3a1ccf2e5aefb514fa8ea`  
		Last Modified: Tue, 18 Nov 2025 06:05:46 GMT  
		Size: 15.3 MB (15318677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a948a2763d8f2241372073b135fe9b93ddfd3cae0caa5dd8e6b36de63007f`  
		Last Modified: Tue, 18 Nov 2025 06:05:45 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96d80de17bed7f17c3423931ffb43517232842f91795ba8013ce68f9070a9169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c727d791365b5d42d03506812fd2b9b0be4f934a376d6ca7e4325e38f0a78328`

```dockerfile
```

-	Layers:
	-	`sha256:1c505e1992092cae7ce03df77dbc0244e46049210f40aed4769979d6e22f332d`  
		Last Modified: Tue, 18 Nov 2025 07:50:24 GMT  
		Size: 3.1 MB (3139520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da0319b2c30a8d5abc88704089e989cd656757caa36aedf5bb65fe74f60fbb5`  
		Last Modified: Tue, 18 Nov 2025 07:50:25 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5a1135ff27205c91bc7f2e72be8be2d91044d5fc435f66e5aa2880016e91bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102387035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b7c6248bcee1b3a2cb5dfcbafcc9fb2ab61f5a7c72560d423af40d2df93ea`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 04:51:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:51:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:51:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:51:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:51:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:51:21 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:51:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:51:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:51:34 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:51:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:51:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56d4852a11e9fbe13c3d6bb7726cd3eb93a579bdb1c230ccb0eb5d112a3a9a7`  
		Last Modified: Tue, 18 Nov 2025 04:52:02 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c666c1482ae3acaf6542d5d4fb32ffbc3b4845dfbf99b41200c887869814`  
		Last Modified: Tue, 18 Nov 2025 04:51:56 GMT  
		Size: 15.3 MB (15305804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0291e7c73badb11de80b343ebaf024ac913a2e4dc13458f71004f6dccc35308`  
		Last Modified: Tue, 18 Nov 2025 04:51:56 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:597d2e4c050d3cf5be17ccc09a6b20286916995ff3c33c1e1b8dc866fcf70745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2f3907b4fea885f38709c043aaad22793c36d46e9301a4fea38f87286c7278`

```dockerfile
```

-	Layers:
	-	`sha256:7f5bfb6bda8f8dd91446b4d6a91519a0016136f0b5764b50e6c3173a4c89f248`  
		Last Modified: Tue, 18 Nov 2025 07:50:29 GMT  
		Size: 3.1 MB (3139827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d052a8c9ea5afe134b7013e474c2189fc6f92e3d879b16d9b84b9698111fb1`  
		Last Modified: Tue, 18 Nov 2025 07:50:30 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
