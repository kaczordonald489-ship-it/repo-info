## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:15020deb417cf28df8ef10ca77aed1ac50bd681c8485d2a8ba39275ba5b734d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79df6fdbbd43aca748da32615369cfd4e3f4a1b0a8853690d505c7a3baaf11eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207921281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d829790959d954f71d4fe9bc0978f8bf1f0693184a64adfa2808eb050c77ec2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:12:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:12:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:12:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:12:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:12:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:12:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:12:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:12:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:12:36 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:12:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:12:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:12:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:12:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb477f45eb91037d12b1b59b92b0d8ef6bef70b15ab2f2b055f1ede3522240fe`  
		Last Modified: Wed, 19 Nov 2025 15:46:47 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572cac7f32bc8b5ea58219601c941519a4f747ec4dea8c7ba3c990993058a9`  
		Last Modified: Tue, 18 Nov 2025 06:13:07 GMT  
		Size: 15.3 MB (15318706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a6899401283918225539b772ae27b18d4e3259aa8915f755b57fb81a5538e7`  
		Last Modified: Tue, 18 Nov 2025 06:13:07 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbf5fcea1900298e2ee16281fb82ff023d1d6c95d5b21fa4a269222a733f755`  
		Last Modified: Tue, 18 Nov 2025 06:13:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:303150b64cb9a206d864a66f8401928bb6f1ad32096d1f7318f4a5a8398b61f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baa53e1233bd32350ef518d8252eb156bd97bbcde5caaa5d752311eb6f346ca`

```dockerfile
```

-	Layers:
	-	`sha256:b24bd3ab5d41e06dc48c7fb6259520b9853ebb5fc226823d28fafce4b0981026`  
		Last Modified: Tue, 18 Nov 2025 07:45:00 GMT  
		Size: 3.0 MB (3021012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2056d5a5653c1b6ac110ea48bdd66acf126a91f108a3c089f4982c8b07ffb3f`  
		Last Modified: Tue, 18 Nov 2025 07:45:01 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37cce41fccfba456bbc1a0fa536c61fdf4bc5a2f4b821456e2d22a1b134f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204679994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ade8330ab710feb1c73d13cbfa73cfe8edd84b1fae8b2499cae0a092394efa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:07:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:07:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:07:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:07:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:07:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:07:32 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:07:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:07:44 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee76f87502e598c395f58e6608ad4dda3eb0275b9cdb19fbf0d6910fbf3254`  
		Last Modified: Thu, 20 Nov 2025 17:18:53 GMT  
		Size: 156.1 MB (156107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5bf81773c3220c11d75b5450b83083840c33f4cf4da537a0f145baf018c674`  
		Last Modified: Tue, 18 Nov 2025 05:08:20 GMT  
		Size: 15.3 MB (15305767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec7caca8debc9bae0325d8a39d2ef25b921bb29d41640fcc32274e1f8ec32d2`  
		Last Modified: Tue, 18 Nov 2025 05:08:19 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890018e7544270c131c1f5197287ca3c174db953b445fc5fa6de775b96253002`  
		Last Modified: Tue, 18 Nov 2025 05:08:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a3cf901aebe3d9902fc0d515b7be583a479b0608bd15ce5307c0b741fae3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18eccc5b1bda88e31ed11075b4b1d49762f9db1b67491b80992b279884c6c6e0`

```dockerfile
```

-	Layers:
	-	`sha256:71fca4a6b3cb0752dd1ca0541c632f94ea25829d687689325d1d9ffc1f20bd3a`  
		Last Modified: Tue, 18 Nov 2025 07:45:05 GMT  
		Size: 3.0 MB (3020621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77419a6415b0de53d29ea3e04e04608c4d6c06cedcf2f6efd1114c94bd6b195e`  
		Last Modified: Tue, 18 Nov 2025 07:45:06 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
