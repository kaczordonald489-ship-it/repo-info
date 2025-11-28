## `clojure:lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:f7a1928e70aacb1b574fc274f71168bca492bf9dbad4ee2a17c8eddb1848e531
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:90b530897ac0d0aa2df865d937a6ecbe760dcc632b45027c979b677acb31a0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166927488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91934c2ebdc4f99a3f3fbf4b3c8fe14b12a965154bcce94a29fed4d6989227e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:15:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:15:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:15:55 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:16:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:16:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:16:09 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:16:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:16:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:16:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2cfad889ec881e43016a180e520464f2003fb9fea872dfe7f83b4f8318be13e`  
		Last Modified: Tue, 18 Nov 2025 02:27:51 GMT  
		Size: 53.8 MB (53756431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fabda67223a4194fa3462816183ec80e6a4ec1fbc8e1b42476a06147808823`  
		Last Modified: Tue, 18 Nov 2025 06:16:42 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38032d827be0ebb83fda3b527464a96bfefb96fd46e1981ad494a8d6d237c078`  
		Last Modified: Tue, 18 Nov 2025 06:16:37 GMT  
		Size: 16.6 MB (16607569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82a4e9fe5534e8f4e2382a6dcc8c5e6e2b51912baa086a2805db8f09443de5`  
		Last Modified: Tue, 18 Nov 2025 06:16:37 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d61109771330c20853b12b0ea063a29031b683e1b1a3fa84078b7c5c2570cd`  
		Last Modified: Tue, 18 Nov 2025 06:16:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8fb90ea42faf823ca880bf3b1e1ce2a47c631a6fc6fd138296f3b60e393d8bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a4a4d592388ccbe6b0c9a317cd9578b8fed8ff44500118f24d9aa176e25fc`

```dockerfile
```

-	Layers:
	-	`sha256:1494d8a5cb365ba1c17584186446d6941ee52c39297dd2526e244242c0ca283f`  
		Last Modified: Tue, 18 Nov 2025 07:36:10 GMT  
		Size: 4.4 MB (4427494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d4c2571a245f240bb68c149caed3661306fff80dbb459a5e70edde3a26a8ab`  
		Last Modified: Tue, 18 Nov 2025 07:36:11 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8755f6d496e9d1ea158473208b57ba4458087ca67065cde16bf22e19dd8c9c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164423343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ea0eca66fd1e2759220f0609ccc4594df8f348527650c386cc977649b577bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:12:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:12:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:12:54 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:13:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:13:08 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:13:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:13:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:13:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:13:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d3d88c171e228bf518ae34b2ab7dc7c4ea00ec7d81ebc15f3c2a53e89e942f`  
		Last Modified: Tue, 18 Nov 2025 05:13:49 GMT  
		Size: 91.1 MB (91052501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fbab3f5ce2eda8d2d58009fc0fe2ad3349fb37af522925b6a3fe0de7fb5e55`  
		Last Modified: Tue, 18 Nov 2025 05:13:40 GMT  
		Size: 16.6 MB (16595013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b755ce3f15ee5b6ede67a858c5096d34e836945d78944ff058fd8df10582c50`  
		Last Modified: Tue, 18 Nov 2025 05:13:39 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf2bb83333a029e7b0c8e98f84d06c87f0334b2ba5349405e835cf02239cbb7`  
		Last Modified: Tue, 18 Nov 2025 05:13:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aebec66c8fd0f61eeecebf47121edf53abdade50876680232909cf5d29e0ebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1d063e1924baf3d87c8ef39c8c8175df090fe41c7fac26dfe2f829927b3699`

```dockerfile
```

-	Layers:
	-	`sha256:638e295b897397c86de99f53ed49b2ab946f2d588737596ebe56c2d2a9298cf5`  
		Last Modified: Tue, 18 Nov 2025 07:36:15 GMT  
		Size: 4.4 MB (4426489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a71d110ade80e10e2628ac6f060977ca2253d6ba09cbf3f461b37648507d52`  
		Last Modified: Tue, 18 Nov 2025 07:36:16 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
