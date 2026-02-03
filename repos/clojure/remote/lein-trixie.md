## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:86fe60b860a0197097140e8f3d33d43205e03ac710a8882b5cd76c9ea4897cdd
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0c505315be5af4d8ea71a8a5a714ed010576183f9a375200c7a35b92b1eb1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164436481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a9d0492c6596e29cc1ad1856481c0b003991ffca2a27a64e9f1c8df900b6ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:22:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:22:36 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:53 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4f8a9b8dceb30f133ef0dcf605943642e4abf5a653801627ade54e2f41ff`  
		Last Modified: Tue, 03 Feb 2026 03:23:14 GMT  
		Size: 92.0 MB (92045315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f6c89d2d8670de0783ab9e7c62def9524c607a7ccd2875479b393d4f0ed3f8`  
		Last Modified: Tue, 03 Feb 2026 03:23:12 GMT  
		Size: 18.6 MB (18580040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb32339dd3d659971f16d08309c8607949a3339c11aacfb1f916d8d661655a`  
		Last Modified: Tue, 03 Feb 2026 03:23:12 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe40d85e29c92f9489ccd6372eb608540987b146af5697c78dfe6008ca60a1e7`  
		Last Modified: Tue, 03 Feb 2026 03:23:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c5726ff53886cdde7960bbb1c3959d8885499d21608a55a239b9a3147bac12dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bc5f0726a62c2a47c57820bc666dbe695215a7fb6e7ed0e194111c10af65d3`

```dockerfile
```

-	Layers:
	-	`sha256:60ef122834b9393700c7527be732e29a6a236eb47c707677dc3ff9c81167aaab`  
		Last Modified: Tue, 03 Feb 2026 03:23:11 GMT  
		Size: 3.8 MB (3765535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f2182b3877a2d665a37eb158bd68d89fa65f0f6c43f4ca1a09f51921dda044`  
		Last Modified: Tue, 03 Feb 2026 03:23:11 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53e280b08d82039cb8f7524260eaafe681aecc335283991a3a8f09847ef8b108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163764089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e1d05c441a59bf09fa0ac35dee2b4283d2f846cd7f67c465f34bf5306b5530`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:25:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:25:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:25:10 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:25:28 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:25:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:25:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49730293cbc0cdd5594518891c148b60432c5bc0f45905ebf34f7f9555539b2d`  
		Last Modified: Tue, 03 Feb 2026 03:25:51 GMT  
		Size: 91.1 MB (91052483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fe5850639fe866601bf469cdfc50ea2ba855deebc23addd51bcc8533b91fb4`  
		Last Modified: Tue, 03 Feb 2026 03:25:49 GMT  
		Size: 18.5 MB (18541459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c86664ab6774feae56b9866fdb3f3c199145404f86c4c0c0611f2b093fa7af3`  
		Last Modified: Tue, 03 Feb 2026 03:25:49 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bdfef2cf9a868b47035a98f246a39280ebdd44dfafba071b49f946994dd4a2`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c4be39e5b6e3897dabcc4b6ff1ff10e21f06985ecad5bde92e96812a0f336984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917bcc9a135fffae4e1b58c4ec272af1ae4e6e9cfa869c66ea612e628d76e4be`

```dockerfile
```

-	Layers:
	-	`sha256:594463df789057cfcd6629098ab1beb229f62c9897bedcfb8629783b84599d0c`  
		Last Modified: Tue, 03 Feb 2026 03:25:49 GMT  
		Size: 3.8 MB (3766433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45b41c5be51074ad59c750cc7ef4142525c62f99b2a2108e511ceac9d4e1706`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e94456761cea43d8026342fd2e1fea47a9b7f3af76a4a280cd11632245431e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167873226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0ed8b9957631c5df99541e87c8a97cf622689358ae9f3d3ad345d2d5d1cb61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:39 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:44:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:44:40 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:45:48 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:45:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:45:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:45:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:45:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1f64ed71cadbfa0fdd0e4e5f9f9173c20301e99b8d557346b7aeda0ac3389c`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 91.6 MB (91610765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17de3c92287919744b3896a502651763254b80443ce4025570cb8d29b7d9fdd`  
		Last Modified: Fri, 16 Jan 2026 03:46:38 GMT  
		Size: 18.6 MB (18637316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68b67140e39db4d8a9e26a20d33bbc7d2fe60a73644040efdfb23e746d7fc9c`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c169d06b9f82c8bb796c446fb810d6ef6583bb58806ca25768d275487220514`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb38e3290ed4f0ae62d0ef02cdd61a876277c5e116e34e2035ea875a2612e9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7945d60dda0220177b3c81ede2141760c0def9b5d02e12584a92398067d85947`

```dockerfile
```

-	Layers:
	-	`sha256:11a860115e4f50334dfca3588c4e50699092db65b7580bd6ff2ab60e4b403463`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 3.8 MB (3767845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8984339237b90de25dad371d70c0ebc0db6c7ee57e91091821fe5a018ac623`  
		Last Modified: Fri, 16 Jan 2026 03:46:37 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:277ce0e3d3699fa794ea22619b2d4d55bfdff5f10bf9d489f745204d47cdcff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156f7d283f2601a985ab30188f3e94cb80f55104b6a4bef287108b1ec4ee2cdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:29:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:29:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:29:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:29:57 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 22 Jan 2026 04:29:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Jan 2026 04:29:57 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:31:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 22 Jan 2026 04:31:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Jan 2026 04:31:27 GMT
ENV LEIN_ROOT=1
# Thu, 22 Jan 2026 04:31:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 22 Jan 2026 04:31:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:31:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:31:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68915c625875c7ea3b1992ce94ece2c2d543657883d1675eb2625132930fbabc`  
		Last Modified: Thu, 22 Jan 2026 04:35:23 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f2a0896a57927db666b336f35acaa7313c269f176c919e4f34a21d94233ba7`  
		Last Modified: Thu, 22 Jan 2026 04:35:13 GMT  
		Size: 18.5 MB (18531720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47df26baa9ab0ae7043661e1ff2211fc9beb15c899c46d60101ff0d4e524cee`  
		Last Modified: Thu, 22 Jan 2026 04:35:08 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88b8d36a3e8e8a8a52af31f6f2faac052af3424d279b5f1d2cb4a0ebc15bafe`  
		Last Modified: Thu, 22 Jan 2026 04:35:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d01279e35f39fbb9d6b877ecb707c96a9bf32e4906f1ebb117be8c18cc253330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f07dee3ff125b61d25dbeb4ff882af4c6d0e6f4ffe283685cad7d2de127d0a`

```dockerfile
```

-	Layers:
	-	`sha256:8033ae8628aba07cfd6f2a1ed50b445efa5dcb96da8966a0858d763083a9be3f`  
		Last Modified: Thu, 22 Jan 2026 04:35:08 GMT  
		Size: 3.8 MB (3756021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869613899b4bc31e39b17fa1356a9d1341569a6deb274bbe79dc7f2355d890f5`  
		Last Modified: Thu, 22 Jan 2026 04:35:06 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cc28849186fda4c7d79e2a3ae22ccd1178ecd9c3c006196282a817521eb85d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160704232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0998cd309d0a5c77a8c5de188d822a2563ab5e5e8d6920c3985bd60ae05e80fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:03 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:06:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:06:03 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:06:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:06:15 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:06:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:06:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44692e8f5993370045053829da7afee7b337c7a2e81c01f2c2132ff813e3d17b`  
		Last Modified: Tue, 03 Feb 2026 05:06:43 GMT  
		Size: 88.2 MB (88210678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b327f18f1af0e2cf51d45cf047f843c2935d86676db4fd543fe59ad10c5d677`  
		Last Modified: Tue, 03 Feb 2026 05:06:41 GMT  
		Size: 18.6 MB (18621022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681864e2b80a57eb9b4c01bde19ca66559d48338df723c18db38370d1361ba78`  
		Last Modified: Tue, 03 Feb 2026 05:06:40 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d3de186552b59eed75a165a728a92ad3e159b1b1521bd81755e2778cce808e`  
		Last Modified: Tue, 03 Feb 2026 05:06:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2fe2cff98d3a098bfd774ab8b26e09d2c7547db9436dc3afd365b004d217f58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46cdbe2b26e2d8e8e2c6ccf6606e08c0335b3ada9fd417228626b8936103ff3`

```dockerfile
```

-	Layers:
	-	`sha256:b978928890fc61fec9400b96a0f0e5a65d516ca5134ac2632880b7b0bee84d32`  
		Last Modified: Tue, 03 Feb 2026 05:06:40 GMT  
		Size: 3.8 MB (3764510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88709d5b1455748074007960f162b3d48e0c56268dc03c42a3dcc92ab80ed96`  
		Last Modified: Tue, 03 Feb 2026 05:06:40 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
