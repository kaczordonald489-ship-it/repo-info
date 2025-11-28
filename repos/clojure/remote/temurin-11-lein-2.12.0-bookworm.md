## `clojure:temurin-11-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:013c3073cdee65ce86693358936e6eb73c54f9690095b3c2dfd436e60141634a
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

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0abff1cbb0ed4e622d51bd8c4c2a454fe3af6b9d4626be93a4a18aaec4e3ac5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217767995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26f8f0df4ec338bfde6860139f333ea9ac6ff189dfec0444d8252ac3f09b777`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:06:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:06:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:06:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:06:38 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:06:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:06:52 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:06:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:06:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85bf2bb3f6a55f75d48be786e9872be3a93c93d05d8709dac2645a06118e1fe`  
		Last Modified: Thu, 20 Nov 2025 02:54:52 GMT  
		Size: 145.0 MB (144966634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7456eefd6950699ad46a1cf4f9b8613c5603ab3a52ab75d628acfe75c699dcf7`  
		Last Modified: Tue, 18 Nov 2025 06:07:21 GMT  
		Size: 19.8 MB (19802824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799cec3a6a5fd8701aa395da3b20615b1f9d42f2d8965c5b8379ea5e7ef1a7f9`  
		Last Modified: Tue, 18 Nov 2025 06:07:20 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6702931b75b93d8a6c2c0cb81e71c07d7c962ad9bc24ecf57e1203c41e8ec731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4636e189a5d9406ef43177e9b6b521efc7737b19410292b7c44848dc4182e0e4`

```dockerfile
```

-	Layers:
	-	`sha256:12fd63d38928779e76921f2f45d0dae9d65b2cb4e4623a2aceb53297e24f5a38`  
		Last Modified: Tue, 18 Nov 2025 07:37:57 GMT  
		Size: 4.3 MB (4299975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e56f7fd524ad741b3804ca8057c075865190b16633e835a8bc90bdd29cc9f3d0`  
		Last Modified: Tue, 18 Nov 2025 07:37:58 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c1cedd9156b056b8ef641535fb5b3171702686e1fcba0371ddc92d8d51d47ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214240612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d15aadc6dc9877967795428ec027a283f2ea9eab6553c14a1fde84a545b9cc0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:55:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:55:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:55:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:55:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 04:55:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 04:55:58 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:56:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 04:56:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 04:56:12 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 04:56:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 04:56:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbba4b5971ea71d22615d5fd4ed396688d72f8b00ccf678d9fd74aec658f062`  
		Last Modified: Thu, 20 Nov 2025 21:38:04 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bd82c150d15a0844993221ee0b1691568798665d800206151e5d2b3ffed9dc`  
		Last Modified: Tue, 18 Nov 2025 04:56:43 GMT  
		Size: 19.6 MB (19632118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7add7abf0670f1d749ad820dce945a0dc5f8eb77450e7c96dcafab17aa494d7e`  
		Last Modified: Tue, 18 Nov 2025 04:56:42 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e4fd421f328c6e3733e15dcf0fa83f6a46555a07cec20c0aec42d47722f2526d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b095fb6cf3035d5c0386d547a657c8f3971fcc5c23190e58adaf8a59954f34c0`

```dockerfile
```

-	Layers:
	-	`sha256:94df4e7d6230855ed1fa344169fa8d7c0011b4ebeb0e9eb23eea18230d873509`  
		Last Modified: Tue, 18 Nov 2025 07:38:02 GMT  
		Size: 4.3 MB (4300208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b61241653c65083a3b6ad685858450468ff1bcebae54c9d9c40ea6fa5e1a87c`  
		Last Modified: Tue, 18 Nov 2025 07:38:03 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa2b4e4af2326a07e5eca0ef609fd504692e1eb4486a8d7166ab3c8c7db417e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208948472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04746d2991f04109f49632f20287ef6715f7949d81689cd60481c8780eff3a8f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:18:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:18:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:18:27 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:19:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:19:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:19:03 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:19:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:19:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764da875785de8387fe160895a48fd21f77d1235503a9bb47628ccbcf6e2015`  
		Last Modified: Tue, 18 Nov 2025 06:19:50 GMT  
		Size: 132.1 MB (132081985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfabfb1d664d555502c0139e585eb04c174b877a02c3746bcd3f01ef39a8a516`  
		Last Modified: Tue, 18 Nov 2025 06:20:01 GMT  
		Size: 20.0 MB (20021747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb135a0764c5bf1db4638a87dacd78e296a1bcb7df15e77deb0a9aaca9ce85`  
		Last Modified: Tue, 18 Nov 2025 06:19:59 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d939b3889bd305ec7a4e2c8f17bf3d2874552d45cf674a9bfaa159c6505749f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375b79d96d25d914010f2c0eda21c0d210e0add6afd513fafb8d4fa95147bfda`

```dockerfile
```

-	Layers:
	-	`sha256:c0f8581987f94187e8bf2097cc3e75a62b6bcfe431d02eb7dc0fa05029f8750e`  
		Last Modified: Tue, 18 Nov 2025 07:38:07 GMT  
		Size: 4.3 MB (4301219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc57eaa6e3f0d180485aeb4888cafbedcf07cc8c77cdf78c1b5c000565679790`  
		Last Modified: Tue, 18 Nov 2025 07:38:08 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ec118a239e805fff801db176e55e5dfd4086097b76cf1ff1feb358e0947e6322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196810653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0778e7473ecc5bcb241cce569f03e49bfb0251a6eb6f89f345916703b1b66055`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:21:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:21:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:21:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:21:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:21:57 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:21:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:21:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74edd87eeef1ca4a456ef8951738a1f7f0691267d689c5317df1e6091dec4952`  
		Last Modified: Tue, 18 Nov 2025 05:22:41 GMT  
		Size: 125.7 MB (125694447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146a4d2bb04cc28522dfad92eb0402454781a9a91099ebd8388bfb37677afd6d`  
		Last Modified: Tue, 18 Nov 2025 05:22:29 GMT  
		Size: 19.5 MB (19460780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a66095b629e325e55fe4f8d33539f34be7f2eeaed9653ce428899e85ce4fa48`  
		Last Modified: Tue, 18 Nov 2025 05:22:29 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c6bb012922b44fad4188c35ff1db65a9121c7af0407b1d251a3416eedd930d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cc18cc29b6c25f0b1f33fa71f3ec160c9fbdc675ae043b74950356f0cc2f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4ab242c619df1ddf194bff5d83a45c4c24f18d9bb1628ee3055ffb3fc879447d`  
		Last Modified: Tue, 18 Nov 2025 07:38:12 GMT  
		Size: 4.3 MB (4291793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f727e25608b8d180f9ed300453870f82c7e7c774f1dfe8aff7fce000b254934`  
		Last Modified: Tue, 18 Nov 2025 07:38:13 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
