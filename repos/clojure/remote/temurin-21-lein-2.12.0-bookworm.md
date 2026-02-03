## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:39a678ccc31dcc74f438903ccdabdf197dd708579c83a639c030e94f1d788330
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

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5fe50bf3934bd15380b4a59b4ed10a1ac98f99bcd5411f878f3d4bdcbffec742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230628559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2679c4b84bfd4e5416643fb2f1eb88bc4ccc28472e690552810d3a626e743861`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
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
# Tue, 03 Feb 2026 03:21:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:31 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860b04ce7d570cf5693b9163257d6d56bf0834c17b17f61b8dbf0861b293af1`  
		Last Modified: Tue, 03 Feb 2026 03:21:54 GMT  
		Size: 157.8 MB (157826057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ec758e9786a47f076e126eb0c122846765fa676009c5eeac93bb36a74e9163`  
		Last Modified: Tue, 03 Feb 2026 03:21:51 GMT  
		Size: 19.8 MB (19802874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f625f996ada88d09b7171db58148024a3c838ae315c25a5b73ec6ec27031b5`  
		Last Modified: Tue, 03 Feb 2026 03:21:50 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efd230ae885ef54dbccbacbd2c53e99623fb8a7214d2514275b2dabf5a8e1f`  
		Last Modified: Tue, 03 Feb 2026 03:21:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:953c716d15e152e4cd144eda1d870ec5d99a382850ac1dbb654af96cab00bfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f29db85103f94329a69235b66a4ad160caabb51524ad7c50128438095c2c35`

```dockerfile
```

-	Layers:
	-	`sha256:1d748951a97f32c0ecb5dbc65dcc3b44c2c92721500b6ef7536888309df96744`  
		Last Modified: Tue, 03 Feb 2026 03:21:50 GMT  
		Size: 4.3 MB (4284231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6dd8024d7451a01b83205c412251d64bcdfb74aa97dbd3f1fbe4a7c4b0b143`  
		Last Modified: Tue, 03 Feb 2026 03:21:50 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d8107ee88031a4993a65bb1546e09af905461aef077bf7e92fcaf15c0bb506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228624511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6184d393f1f26e66c2e17fa34d7f324ae4d444ec4d1e442b78b4f9258b350a38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:43 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:58 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465700d6c9562f42e5b220884744eeea9b6380ec89fa0bb250109e0101af48d9`  
		Last Modified: Tue, 03 Feb 2026 03:24:21 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8100e5cfee15fa3a179116712b3498a9af99a3e6aac9b7f260a6b0163d3d0640`  
		Last Modified: Tue, 03 Feb 2026 03:24:18 GMT  
		Size: 19.6 MB (19632794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cab3980cc20f502cb967a6f6ecf56f95712291f1077e628eac307035214827`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac817c6d513e1cfdeddabeb42e87707278588784ac234c39c72f37c4ad834d4d`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b78d9390f81ef7952e0fc4246503de38eecd7f2bdef4b4e370e6fba2613a97b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a177ee7b001d519b392f82aa259c27af849eed76caf88ca6f886eaab9c0a6a`

```dockerfile
```

-	Layers:
	-	`sha256:81d1699d78227abf77d8a177d857cbdbce25f60239ce12130e94beb749801537`  
		Last Modified: Tue, 03 Feb 2026 03:24:18 GMT  
		Size: 4.3 MB (4283870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebfd925444e189eb4025035a1cf7dd569fe542af9fc7c6f4c7079f6d2d68147`  
		Last Modified: Tue, 03 Feb 2026 03:24:17 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ada8bfd9abfa7ecf466306635c136dbf59c42ba46b0bc6b0c5c0b65074e9b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234811026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6a20fd511f02a3860fadd86b272a3b915240846295f341001760ce5dd4385f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:28:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:28:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:28:01 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:28:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:28:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:28:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:28:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81e238ae58948d8dc745be1e6898b971765c75d8be7f14150f15f3e10660ba`  
		Last Modified: Fri, 16 Jan 2026 03:29:06 GMT  
		Size: 157.9 MB (157942941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f983a34166d5030b106a1729d522fffeee6b3b73474e47aee8b228bf23b72f02`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 20.0 MB (20022539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d859a52b0f4ef005fb6a16db2f97fec50e92a93954e2227b967c5dc4184646`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f907dcc14128e331dff2f1dacba2d4260334f397d3bb6c4bb6e50871d710b6a`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:050a1f84c961210408c94cbe935ac10bed99d40051e03192bf44695e25657266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8b7a629c02f070951e291debe390033e14198943e859719c49cc12364418b7`

```dockerfile
```

-	Layers:
	-	`sha256:731e9a3ee9092375921ba6af0a4aa7da81b91c7a6dad119005e55618db9bfd8b`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 4.3 MB (4286104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d83e85a386a16bc9aaed5b13e401b8a56f9e8f1c63ba8df0fee7cc1dec681f`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9ca4b6f56ba81e424f5ebae53a4668d423ec419beb77afdf730dda06b3988ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218189557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c9a28392851f34e59341b749684babdd78cdca4f025534c2cd1f7c6a83c4ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:03:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:03:53 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:04:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:04:04 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:04:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:04:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ae753e080cc50ca20884f34f16a7a103d8cdee0bb115b2a6163947581cac7`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 147.1 MB (147069863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dc68a3764d245c2deb1669f1393bc6c98d6ddd0e6656c5f70634edb7fccdcd`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 19.5 MB (19463168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1f222fa5e74c1935de2b91fd5962dc8dc40b8a58f2f7f7f3da15039c1572a2`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bf46bd1e04b7bb59bb340f4126f99602b90a004e237f7c0c342b9c38248934`  
		Last Modified: Tue, 03 Feb 2026 05:04:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ee71d3aca67243d18ca4994de4d053ea7beeb57adf9d94de9d54cf4197192016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f513db4171e4aceef8307ac33b48290a520ee6f0739a1dc6bc02d3829a6ce24d`

```dockerfile
```

-	Layers:
	-	`sha256:50b72b1b108938af679bc76f1e17625c404fa7cb025141fd33e61b24ceed4d9a`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 4.3 MB (4276045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21fcf52a903597978490e26fb748f793ebfba179a70bbac3d19d82af9964ecb0`  
		Last Modified: Tue, 03 Feb 2026 05:04:32 GMT  
		Size: 19.0 KB (19016 bytes)  
		MIME: application/vnd.in-toto+json
