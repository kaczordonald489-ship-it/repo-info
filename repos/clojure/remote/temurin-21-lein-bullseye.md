## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:9039a9212c891b9ea1712cd7cfbdbb58feaf5dbbc0bb169b3a4102e9af771ff8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:97c7bbc09333f6704633a4ea7d2f0e3a2b69bc2cc7dc917041a51d34f4085b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232708002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e20b44a0d3b7ba837e8547d97b7b93c8ac544f0b5e5e8bb431bad9fba5b694`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:14 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:29 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4d0209a6bef39150f62a458e1ab23a63e1aca6d44e8f15d26525df7465cde`  
		Last Modified: Tue, 03 Feb 2026 03:21:52 GMT  
		Size: 157.8 MB (157826056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e148def3534906e68ec47bb1ca112ede5654898bcdbc198c98a6b753366752`  
		Last Modified: Tue, 03 Feb 2026 03:21:49 GMT  
		Size: 16.6 MB (16607553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef70a37e75be561a08666761bb4238a18fd5475c28519ed14a1c9d8354d125c`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf366262ceb5d5887500df3c49734de502c7e35031637efb916abd509d349d4`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f133573bfe3fd29e77e39830ef3e41b2986013f68858fd778fb8a4e950636de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d709fe79ebd8e6fbfabbe1f391062bc271c6bb2218650034491791e58b6a750c`

```dockerfile
```

-	Layers:
	-	`sha256:5e585b64f1ef030e92d36ec42ce675c8c5903d20dbdb46798f6041eb93e48893`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 4.5 MB (4479292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327cea8921e24c433b39f5c11ca3bb56bbeb5a35aafa79d7f639013ff0852490`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e486b7fcd3f30be11c9fe61d86d5b5b3c5be0713509caaf9d87d45c463434d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229479142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cc13644f25a8be31bb0360924b34e9edfd95c21ddd2507773140b260724ae0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:23:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:54 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:10 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fc26e13d6c0693f7829b7fa2d1f59515288efc570cd17dac2dbdf59172270a`  
		Last Modified: Tue, 03 Feb 2026 03:24:34 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869e9070b9f41996aece6d91163d4b3d7c1cd11e47ee239ee936b9236514ed8c`  
		Last Modified: Tue, 03 Feb 2026 03:24:31 GMT  
		Size: 16.6 MB (16595032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b972f783b6fc74baa49aca66c8d0cc5accaab56a61ce1cbe9eee72665e366e`  
		Last Modified: Tue, 03 Feb 2026 03:24:31 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30931f91aca0a55844a2e24fdeb2ef2b4a0db0239a63cf9dd64fbaaa4edf200`  
		Last Modified: Tue, 03 Feb 2026 03:24:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9738201979de951a0d76b88cff3787864e5b35c159c1f1b046ed0ce930ac4d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5201d16ab4023fe1f0fe73c88d5989ed69b1dae8c1a49facfa5fb1f56fae8853`

```dockerfile
```

-	Layers:
	-	`sha256:af985a6cccd0ade37231c01032e8dc86b21845f1276a7587eacfb6679c80cd4c`  
		Last Modified: Tue, 03 Feb 2026 03:24:31 GMT  
		Size: 4.5 MB (4478266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c45c5d221b681ad5ad83ebb11758486f3826180e7c9ee075c98b1675b8fa874`  
		Last Modified: Tue, 03 Feb 2026 03:24:30 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
