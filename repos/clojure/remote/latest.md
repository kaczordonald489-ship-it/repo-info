## `clojure:latest`

```console
$ docker pull clojure@sha256:e86993809abbea724744d85dc70db780b9d8b2b81fcf04dafc0b81c7d7f3de26
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:71aad59a61c7822061f7735b458ac3182b9bdaa27ce6dda64c52130eaf18a009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239920286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69970bfb1cdb61134e0c63858529bde2f07654c2825507607db30d3b0c61cf07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:04:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:04:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:04:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:04:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:04:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:04:27 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:04:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:04:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:04:41 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:04:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:04:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:04:43 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:04:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:04:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:04:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:04:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:04:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1616bd26c6cc8c7ae240b41e4fc0e26aa75e7bc6312fd450089e242b75dce37a`  
		Last Modified: Tue, 18 Nov 2025 06:05:37 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa213be58d23ffe6dd1fad154e801eadb6c893c68c19ebf5dee2e8fd48b8def6`  
		Last Modified: Tue, 18 Nov 2025 06:05:27 GMT  
		Size: 19.8 MB (19802858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba89804ed7c1c2f35edbea15441112b18405b74609e4562cc15ef6b574d83c2`  
		Last Modified: Tue, 18 Nov 2025 06:05:26 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671a093a3d1ec3a2c86b90b2bc73842ffc11bd54e81e6a93d4bbf7ab11e4567d`  
		Last Modified: Tue, 18 Nov 2025 06:05:33 GMT  
		Size: 75.1 MB (75072528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e738f8e641fe2ee0809ecffc9c53ef5ca9e3214605ee0075d9d99dd7c37746`  
		Last Modified: Tue, 18 Nov 2025 06:05:25 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4557cdeda77384553ab7e8e794202ae707dec55532bc92c584398edfa499db`  
		Last Modified: Tue, 18 Nov 2025 06:05:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:662dd345046fcb243eeb8d6785be9607fab1f2586d52f6637816f1955b0d4fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3444005476f92cc024bb4d7e2eb57c12722197a6516d178178c8db0085a639db`

```dockerfile
```

-	Layers:
	-	`sha256:2fbafe4d925cf45b8d7a8188e2222854fee7c7c62428ccde36443a878bc34b9c`  
		Last Modified: Tue, 18 Nov 2025 07:35:29 GMT  
		Size: 7.4 MB (7418725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7376aec28276e69bbd60099c05ab3b950335258ee9ef61d56859c48a457892`  
		Last Modified: Tue, 18 Nov 2025 07:35:30 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc2ce4068bf96123ba951f83c60ffcfac37836122d6cdfcf2d85509e9e75f824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238688350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069d50480f7320f87b086da5e654ba47ea2c25695cfaf84e158a6f9c1e258ffb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:50:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:50:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:50:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:50:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:50:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:50:13 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:50:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:50:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:50:28 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:50:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:50:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:50:30 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:50:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:50:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:50:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 04:50:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 04:50:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362bdf1f308e383bc6819a4594948e200353305e2c24a56fc60fac5ad8b0c964`  
		Last Modified: Tue, 18 Nov 2025 04:51:30 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36460dc22919d5e64bfa638e3548e1e7c96b6c538e8b1680187b9d68fbe6943`  
		Last Modified: Tue, 18 Nov 2025 04:51:15 GMT  
		Size: 19.6 MB (19632176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b75c33922fee191b87385079155eb16ec06db3a3bdec8bd68e5e57faae7e1d`  
		Last Modified: Tue, 18 Nov 2025 04:51:13 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2dbe00676ad7cdf323015052b7b5e8aba960cb3ba10adbc056c73da572c5c3`  
		Last Modified: Tue, 18 Nov 2025 04:51:20 GMT  
		Size: 75.1 MB (75125747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc53182ec48c9e760d3fa41be4a8c64f2b02d6b8e6aeb724372f9852083ccdf`  
		Last Modified: Tue, 18 Nov 2025 04:51:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f220b3ac7483cbea9a1db4c539ff066ac4e17c79ec797b3ffcf6c8ab997e044b`  
		Last Modified: Tue, 18 Nov 2025 04:51:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:b34ac8580734f6660502c0670eb05ba180486b1df584527d4df6e9ac719686e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d391b934c739d21c7957f84c97391dd9f2a48d00d8c933050b9283ac506d82f`

```dockerfile
```

-	Layers:
	-	`sha256:5d2c7dbe7ae8aea72f5f67e0656a389827604f415cbc250372125ed079ab6a30`  
		Last Modified: Tue, 18 Nov 2025 07:35:35 GMT  
		Size: 7.4 MB (7424461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef9f88eab1e46c3c7c5d0332b366642ba9c427ed8230b2afd2f351ae023742e`  
		Last Modified: Tue, 18 Nov 2025 07:35:36 GMT  
		Size: 25.7 KB (25732 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:a66fd9de5e04531f6c98378fffd62ebe85871c5406de67443426880438a157c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249153385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72f918f1d80228f3dd84bcd022799f71190c4454ec92cabd301e2003a0d14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:11:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:11:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:11:07 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:11:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:11:40 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:11:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:11:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:11:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:12:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:12:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:12:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:12:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:12:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42c99d7c799ee7cb4bcd9f016e2e075ba0305357c43f87c1b2db5156bd271d`  
		Last Modified: Tue, 18 Nov 2025 06:13:38 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d544d7e2ca975664c5aedb6a3c6df31c6420e2af3582810953a088eae6d5ff07`  
		Last Modified: Tue, 18 Nov 2025 06:13:31 GMT  
		Size: 20.0 MB (20021612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc751a37c12c4f7d4cf63db767bcc33cb0c18a1a1e811cd40ac357771f88cba`  
		Last Modified: Tue, 18 Nov 2025 06:13:29 GMT  
		Size: 4.5 MB (4517769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a68f1ec3e8d895b9c6a886c88a048690795ab5bcb38e2ca5c9bca591dfa059`  
		Last Modified: Tue, 18 Nov 2025 06:13:34 GMT  
		Size: 80.7 MB (80675176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ee8197c1ab0a364d82bfb4bd6e63368c5c64d8f6f3326a5c5e5e4d1cbfeb6`  
		Last Modified: Tue, 18 Nov 2025 06:13:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960fe30d50ff5a874b70efc4e5017e7a4c9adfebeb6e06e320eeeb5111d3833d`  
		Last Modified: Tue, 18 Nov 2025 06:13:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:e8a39f6fa9fa359aefbc661a14de9948782101a8c23a4d9a5a2185e8a1dae103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c111ab4d3a6a9619e0f6f7af8479004a58d190575612d9a8de3bbb2c52f79f3`

```dockerfile
```

-	Layers:
	-	`sha256:467aa99dcc7db0d723db01b8c0854dc6d253296833e8b946ae7ec2abb286f1de`  
		Last Modified: Tue, 18 Nov 2025 07:35:42 GMT  
		Size: 7.4 MB (7425225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d0eee6525fba7dada93bb92224c29608a2953b57d285128ac7cf1321f4aec8`  
		Last Modified: Tue, 18 Nov 2025 07:35:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:d47b3dc197e46411b7f803e6746ee69abb2ea20c47e861c15b1a9727bceb9cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233549979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c4b734994ee60a1321d54b97e392b134aee3e6ec4f235cd3cc5c401f2fd05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:21:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:21:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:21:07 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:21:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:21:16 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:21:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:21:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:21:19 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:21:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:21:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:21:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:21:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:21:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa22c8373b8566c846a7e580361bbb86bc05dc4c1fd3498c8de8ba025ecfb1b0`  
		Last Modified: Tue, 18 Nov 2025 05:22:11 GMT  
		Size: 88.2 MB (88210740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e270a59c4ae54170eb18c7e8ad6bc0df7908096a95c2ef80742aeb24c4b8c`  
		Last Modified: Tue, 18 Nov 2025 05:22:07 GMT  
		Size: 19.5 MB (19460725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53200e2cf02a4d25011b2e6837c04c28ceb7cb6aedbd7dcff3412b0a39f1e1a`  
		Last Modified: Tue, 18 Nov 2025 05:22:05 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5f113bbf12c2a60333580502f6b3e286b5b7a3a1f2461cd9820c61d6d7542f`  
		Last Modified: Tue, 18 Nov 2025 05:22:14 GMT  
		Size: 74.2 MB (74222037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5a74783629cf7a1972a54fcc8d4f4343315fb34b26191790fbd7fa691da02e`  
		Last Modified: Tue, 18 Nov 2025 05:22:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36895ca5b03edb159547660065935cfeea197d4438b3503341933e6f1febd95d`  
		Last Modified: Tue, 18 Nov 2025 05:22:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:61c559da121336766b13df75d2512c40c0c1d901c4c13144ceb85b94e9f838d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a26c45ccc15906e5d90317aab4580ef3cced6a28ab25ef548759df2f3d34bb`

```dockerfile
```

-	Layers:
	-	`sha256:732a78e42b7bf5bae90c060c375752b2e24269b9ba320b3365523f2c751ff22f`  
		Last Modified: Tue, 18 Nov 2025 07:35:48 GMT  
		Size: 7.4 MB (7412592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ca3bae07d58e74ff3609dcafffdce462b9278cf6df7ffd9b88c17e5b40febf`  
		Last Modified: Tue, 18 Nov 2025 07:35:49 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
