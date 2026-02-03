## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:26f0174cfd32ef8c3d765d1cd0d6d7af22229a896e978fc90315d98dc21aa0c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0c51d61b09b46cdb2d60f80415c53c6c19902bd40adb6946ffde570d53f9a18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207921248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7692bc6ddb2c5e0337df35fc0193113641fde17bceeed91ed7f991b6c389b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:28 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:43 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa160ca18971d742f7f688ef02f536dfe056881c4ff5c5794736740ee2a8389`  
		Last Modified: Tue, 03 Feb 2026 03:22:04 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ea6a32e421fa24f6a329fde7a8a141d754aecc7299ece2fd1f89bdd5be959f`  
		Last Modified: Tue, 03 Feb 2026 03:22:01 GMT  
		Size: 15.3 MB (15318745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ed928deb9b6d504e8e7a7d0fee067c3db964fe7d8ddb7c04ce80707a8eadc0`  
		Last Modified: Tue, 03 Feb 2026 03:22:01 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba22c4b3a22d23adc6efef1ea52e272b0e8e93406071b2b26ef31969ec7fea93`  
		Last Modified: Tue, 03 Feb 2026 03:22:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3403fa056d496aa02d4a04e4880faa09f8da4eaa7e94a106f088f6e91d2a3236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609a6d940fc870e07d2c1b94a21e03a1b948df5144e59b60e6148a3fd3b16001`

```dockerfile
```

-	Layers:
	-	`sha256:b722e98c20c3c3557461f9ace87d6aebbd4a4051cd6640486c64422936fabcec`  
		Last Modified: Tue, 03 Feb 2026 03:22:01 GMT  
		Size: 3.0 MB (3021012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca0bcb8de6507cc782a1e169cc4dd99a134f51b152a5e8eae049861fa6f1b09`  
		Last Modified: Tue, 03 Feb 2026 03:22:00 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:52769512172f31d1391b7c8e5606ddc967d37569060f703e64ae4ab45aca9215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204675934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b674f854e0621146e66d0848a576a53ece4ee0ca4b4d52461a8fc9105f0203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:49:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:49:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:49:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 02:49:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:52 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6e74c6e4d25b0782b574b670fda91f2431b30e00b8d92ca55bbfb2a8f1ece0`  
		Last Modified: Tue, 03 Feb 2026 02:50:19 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a0c4f0629e466a448620031509a17a787e0daec65c1e3e91bb2e3959d41a25`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 15.3 MB (15305780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e01497771628ac951516b650e9f77a6ffdfd52559bb29f9ba3cd8ed9857769`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0253430a39875f77f1fd7cdb664229af523496fecb93b2f95eb779ce5846e99e`  
		Last Modified: Tue, 03 Feb 2026 03:24:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f61e4e4c345d1f8e0b33b9f096d4a21377a5ebbf228a32c4f8b997174a3c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba51917b1b95cba38cecb741571accbb0010ac569d25d6f6997c3926cd2c4f`

```dockerfile
```

-	Layers:
	-	`sha256:da1671131211d6a840791e344fc0bb3bf795c7c3e7e0fe61a7ba2319e70ebc57`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 3.0 MB (3020621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fbd080a4a47b61a76656a331805a671026f17e812b3f6f6caa9056393d77733`  
		Last Modified: Tue, 03 Feb 2026 03:24:16 GMT  
		Size: 17.7 KB (17723 bytes)  
		MIME: application/vnd.in-toto+json
